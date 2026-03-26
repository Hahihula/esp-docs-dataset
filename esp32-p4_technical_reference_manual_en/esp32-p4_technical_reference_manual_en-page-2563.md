

```markdown
the Core Interrupt register. The OTG_FS core disconnects and the A-device detects SEO on the bus, indicating HNP.

(b) The OTG_FS core asserts the usb_otg_dppulldown and usb_otg_dmpulldown signals to indicate its assumption of the host role.

(c) The A-device responds by activating its D+ pull-up resistor within 3 ms of detecting SEO. The OTG_FS core detects this as a connect.

(d) The OTG_FS core sets the Host Negotiation Success Status Change interrupt in the OTG Interrupt Status register (USB_CONIDSTS), indicating the HNP status. The application must read the Host Negotiation Success bit (USB_HSTNEGSCTS) in the OTG Control and Status register to determine host negotiation success. The application must read the Current Mode bit (USB_CURMOD_INT) in the Core Interrupt register to determine Host mode operation.

3. Program the USB_PRTPWR bit to 1'b1. This drives Vbus on the USB.

4. Wait for the USB_PRTCONNECT interrupt. This indicates that a device is connected to the port.

5. The application sets the reset bit (USB_PRTRST) and the OTG_FS core issues a USB reset and enumerates the A-device for data traffic.

6. Wait for the USB_PRTENCHANGE interrupt.

7. The OTG_FS core continues the host role of initiating traffic, and when done, suspends the bus by writing the Port Suspend bit (USB_PRTSUSP) in the Host Port Control and Status register.

8. In Negotiated mode, when the A-device detects a suspend, it disconnects and switches back to the host role. The OTG_FS core deasserts the usb_otg_dppulldown and usb_otg_dmpulldown signals to indicate the assumption of the device role.

9. The application must read the Current Mode bit (USB_CURMOD_INT) in the Core Interrupt register to determine the Host mode operation.

10. The OTG_FS core connects, completing the HNP process.
```

## 50.6 Registers

The catalog and comprehensive specifications of USB OTG registers are subject to a Non-Disclosure Agreement (NDA) as mandated by the IP provider. To obtain support information for a particular register, please contact Espressif Technical Support Team via [Technical Inquires](#).
```