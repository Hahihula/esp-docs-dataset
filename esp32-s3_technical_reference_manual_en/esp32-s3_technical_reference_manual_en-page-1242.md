**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Section Heading:**
core to initiate HNP.

**Body Text with List Items and Subsections:**

1. When A-device has finished using the bus, it suspends the bus.
   - **(a)** The OTG_FS core sets the Early Suspend bit (USB_ERYLSUSP) in the Core Interrupt register after 3 ms of bus idleness. Following this, the OTG_FS core sets the USB Suspend bit (USB_USBSUSP) in the Core Interrupt register. The OTG_FS core disconnects and the A-device detects SEO on the bus, indicating HNP.
   - **(b)** The OTG_FS core asserts the usb_otg_dppulldown and usb_otg_dmpulldown signals to indicate its assumption of the host role.

2. The application must read the USB_CONIDSTS bit in the Core Interrupt register (USB_HSTNEGSCS) indicating HNP status.
   - **(c)** A-device responds by activating D+ pull-up resistor within 3 ms of detecting SEO. The OTG_FS core detects this as a connect.

3. Program the USB_PRTPWR bit to '1'b'. This drives Vbus on the USB.
4. Wait for the USB_PRTCONDET interrupt, which indicates that A-device is connected to port and enumerates device data traffic in USB_PRTRST.
5. The application sets reset bit (USB_PRTRST) and OTG_FS core issues a USB reset.

6. Wait for the USB_PRTENCH interrupt when host role of initiating traffic continues; suspends bus by writing Port Suspend bit (USB_PRTSUSP).
7. In Negotiated mode, A-device detects suspend disconnects switches back to Host role.
8. The application must read Current Mode bit in Core Interrupt register.

9. Wait for the USB_PRTPWR bit '1'b'. This drives Vbus on USB.
10. OTG_FS core connects completing HNP process when host negotiation success is indicated by reading USB_CURMOD_INT and Core Interrupt registers to determine Host mode operation, indicating completion of HNP process with USB CURMOD.

**Subsection Title:**
32.5 Registers

**Body Text in Subsection:**

The catalog comprehensive specifications are subject Non-Disclosure Agreement (NDA) as mandated IP provider for obtaining support information contact Espressif Technical Support Team via [Technical Inquiries](#).

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback