

```markdown
Mode bit (USB_CURMOD_INT) in the OTG Control and Status register to determine Device mode operation.

4. The B-device detects the connection, issues a USB reset, and enumerates the OTG_FS core for data traffic.

5. The B-device continues the host role, initiating traffic, and suspends the bus when done. The OTG_FS core sets the Early Suspend bit (USB_ERLYSUSP) in the Core Interrupt register after detecting 3 ms of bus idleness. Following this, the OTG_FS core sets the USB Suspend bit (USB_USBSUSP) in the Core Interrupt register.

6. In Negotiated mode, the OTG_FS core detects the suspend, disconnects, and switches back to the host role. The OTG_FS core asserts the usb_otg_dppulldown and usb_otg_dmpulldown signals to indicate its assumption of the host role.

7. The OTG_FS core sets the Connector ID Status Change bit (USB_CONIDSTS) in the OTG Interrupt Status register. The application must read the connector ID status in the OTG Control and Status register to determine the OTG_FS core’s operation as an A-device. This indicates the completion of HNP to the application. The application must read the Current Mode bit (USB_CURMOD_INT) in the OTG Control and Status register to determine Host mode operation.

8. The B-device connects, completing the HNP process.
```

## 50.5.4.2 B-Device HNP

Figure 50.5-4 illustrates the flow of HNP when the OTG_FS is acting as a B-device.

![Figure 50.5-4. B-Device HNP](image_path) <!-- Note: Actual image not included in text extraction -->

```markdown
1. The A-device sends the SetFeature b_hnp_enable descriptor to enable HNP support. The OTG_FS core’s ACK response indicates that it supports HNP. The application must set the Device HNP Enable bit (USB_DEVHNOPEN) in the OTG Control and Status register to indicate HNP support. The application sets the HNP Request bit (USB_DEVHNOPEN) in the OTG Control and Status register to indicate to the OTG_FS core to initiate HNP.

2. When A-device has finished using the bus, it suspends the bus.
   (a) The OTG_FS core sets the Early Suspend bit (USB_ERLYSUSP) in the Core Interrupt register after 3 ms of bus idleness. Following this, the OTG_FS core sets the USB Suspend bit (USB_USBSUSP) in
```

---

**Note:** The diagram referenced as Figure 50.5-4 is described textually with signal lines and transitions but not rendered here due to format constraints; it visually maps states like Device/Host transition via suspend, reset, traffic, connect signals across D+/D- lines involving usb_otg_dppulldown/dmpulldown signals.

```markdown
Figure 50.5-4. B-Device HNP

1. The A-device sends the SetFeature b_hnp_enable descriptor to enable HNP support. The OTG_FS core’s ACK response indicates that it supports HNP. The application must set the Device HNP Enable bit (USB_DEVHNOPEN) in the OTG Control and Status register to indicate HNP support. The application sets the HNP Request bit (USB_DEVHNOPEN) in the OTG Control and Status register to indicate to the OTG_FS core to initiate HNP.

2. When A-device has finished using the bus, it suspends the bus.
   (a) The OTG_FS core sets the Early Suspend bit (USB_ERLYSUSP) in the Core Interrupt register after 3 ms of bus idleness. Following this, the OTG_FS core sets the USB Suspend bit (USB_USBSUSP) in
```