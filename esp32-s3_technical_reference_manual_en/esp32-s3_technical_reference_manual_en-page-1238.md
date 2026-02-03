**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Table of Signals and Descriptions**

| Signal Name | I/O | Description |
|-------------|----|-------------|
| usb_srp_sessend_in | - | B-device Session End. Indicates if the voltage Vbus is below the B-device Session End threshold. The comparator thresholds are: 1'b0: Vbus >0.8 V, 1'b1: Vbus <0.2 V |
| usb_otg_idpullup | O | Analog ID input Sample Enable. Enables sampling the analog ID line. 1'b0: ID pin sampling disabled, 1'b1: ID pin sampling enabled |
| usb_otg_dppulldown | - | D+ Pull-down Resistor Enable. Enables the 15 kΩ pull-down resistor on the D+ line. |
| usb_otg_dmpulldown | O | D- Pull-down Resistor Enable. Enables the 15 kΩ pull-down resistor on the D- line. |
| usb_otg_drvvbus | - | Drive Vbus. Enables driving Vbus to 5 V. 1'b0: Do not drive Vbus, 1'b1: Drive Vbus |
| usb_srp_chrgvbus | O | Vbus Input Charge Enable. Directs the PHY to charge Vbus. 1'b0: Do not charge Vbus through a resistor, 1'b1: Charge Vbus through a resistor (must be active for at least 30 ms) |
| usb_srp_dischrgvbus | O | Vbus Input Discharge Enable. Directs the PHY to discharge Vbus. 1'b0: Do not discharge Vbus through a resistor, 1'b1: Discharge Vbus through a resistor (must be active for at least 50 ms). |

**Section Title and Subsections**

- **32.4.2 ID Pin Detection**
  - Bit USB_CONIDSTS in register USB_GOTGCTL_REG indicates whether the OTG controller is an A-device ('1'b0) or a B-device ('1'b1). The USB_CONIDSTSCHNG interrupt will trigger whenever there is a change to USB_CONIDSTS (i.e., when a plug is connected or disconnected).

- **32.4.3 Session Request Protocol (SRP)**

  - **32.4.3.1 A-Device SRP**
    - Figure 32.4-1 illustrates the flow of SRP when the OTG_FS is acting as an A-device (i.e., default host and the device that powers Vbus).
      1. To save power, the application suspends and turns off port power when the bus is idle by writing to the Port Suspend (USB_PRTSUSP) to '1'b0' and Port Power (USB_PRTPWR to '1'b0') bits in the Host Port Control and Status register.
      2. PHY indicates port power off by deasserting the usb_otg_vbusvalid_in signal.
      3. The A-device must detect SCEO for at least 2 ms to start SRP when Vbus power is off.
      4. To initiate SRP, the B-device turns on its data line pull-up resistor for 5 to 10 ms. The OTG_FS core detects data-line pulsing.
      5. The device drives Vbus above the A-device session valid (2.0 V minimum) for Vbus pulsing. The OTF_FS core interrupts the application on detecting SRP. The Session Request Detected bit (USB_SESSREQINT)

**Footer**
- Espresso Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback