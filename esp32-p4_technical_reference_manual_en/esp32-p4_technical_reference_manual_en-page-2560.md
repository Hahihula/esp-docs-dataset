

```markdown
2. PHY indicates port power off by deasserting the usb_otg_vbusvalid_in signal.
3. The A-device must detect SEO for at least 2 ms to start SRP when Vbus power is off.
4. To initiate SRP, the B-device turns on its data line pull-up resistor for 5 to 10 ms. The OTG_FS core detects data-line pulsing.
5. The device drives Vbus above the A-device session valid (2.0 V minimum) for Vbus pulsing. The OTG_FS core interrupts the application on detecting SRP. The Session Request Detected bit (USB_SESSREQINT) is set in Global Interrupt Status register.
6. The application must service the Session Request Detected interrupt and turn on the Port Power bit by writing the Port Power bit in the Host Port Control and Status register. The PHY indicates port power-on by asserting usb_otg_vbusvalid_in signal.
7. When the USB is powered, the B-Device connects, completing the SRP process.

50.5.3.2 B-Device SRP

Figure 50.5-2 illustrates the flow of SRP when the OTG_FS is acting as a B-device, i.e., does not power Vbus.

![Figure 50.5-2. B-Device SRP](image)

1. To save power, the host (A-device) suspends and turns off port power when the bus is idle. PHY indicates port power off by deasserting the usb_otg_vbusvalid_in signal. The OTG_FS core sets the Early Suspend bit (USB_ERLYSUSP) in the Core Interrupt register after detecting 3 ms of bus idleness. Following this, the OTG_FS core sets the USB Suspend bit (USB_USBSP) in the Core Interrupt register. PHY indicates the end of the B-device session by deasserting the usb_otg_bvalid_in signal.
2. The OTG_FS core asserts the usb_otg_dischgdbus signal to indicate to the PHY to speed up Vbus discharge.
3. PHY indicates the session's end by asserting the usb_otg_sessend_in signal. This is the initial condition
```