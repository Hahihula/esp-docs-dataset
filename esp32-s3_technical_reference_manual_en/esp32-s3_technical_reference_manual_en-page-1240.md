**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Section and Subsection Titles with Content:**

1. **Subsection:** 
   - "Following this, the OTF_FS core sets the USB Suspend bit (USB_USB SUSP) in the Core Interrupt register."
     *The PHY indicates the end of the B-device session by deasserting the usb_otg_bvalid_in signal.*

2. The OTG_FS core asserts the `usb_otg_dischrgvbus` signal to indicate to the PHY to speed up Vbus discharge.

3. **Subsection:** 
   - "The PHY indicates the session's end by asserting the `usb_otg_ssessend_in` signal."
     *This is the initial condition for SRP.*

4. The OTG_FS core requires 2 ms of SEO before initiating SRP.
   For a USB 2.0 full-speed serial transceiver, the application must wait until Vbus discharges to 0.2 V after `USB_BSESVD` is deasserted.

5. **Subsection:** 
   - "The application waits for 1.5 seconds (TB_SEO_SRP time) before initiating SRP by writing the Session Request bit (`USB_SESREQ`) in the OTG Control and Status register."
     *The OTG_FS core performs data-line pulsing followed by Vbus pulsing.*

6. The host (A-device) detects SRP from either the data-line or Vbus pulsing, and turns on Vbus.
   **The PHY indicates Vbus power-on by asserting `usb_otg_vbus_valid_in`**

7. When a new session is started:
   - "The OTG_FS core performs Vbus pulsing by asserting `usb_srp_chrgvbus`."
     *The host (A-device) starts the application setting the Session Request Success Status Change bit (`USB_SESREGSC`) in the OTG Interrupt Status register.*
   The application reads the Session Request Success bit in the OTG Control and Status register.

8. **Subsection:** 
   - "When the USB is powered, the OTG_FS core connects, completing the SRP process."

**Title:**
32.4.4 Host Negotiation Protocol (HNP)

**Subsection Title with Content:**

1. **Subsection:** A-Device HNP
   - Figure 32.4-3 illustrates the flow of HNP when the OTG_FS is acting as an A-device.

   *Figure Description:* 
     - "OTG core" and "Host Suspend"
       - D+ (line labeled with numbers from 1 to 8)
         - Line connected between Host and Device
           - Numbered steps: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`
     - Traffic lines connecting the OTG core, device host.
       - D- line labeled with "Reset" at step 5

   *Figure Caption:* 
     - Figure 32.4-3: A-Device HNP
     - Steps:
       1. The OTG_FS core sends the B-device a `SetFeature b_hnp_enable` descriptor to enable HNP support.
          - "The B-device's ACK response indicates that the B-device supports HNP."
          - Set Host HNP Enable bit (`USB_HSTSETHNPNP`) in the OTG Control and Status register
       2. When it has finished using the bus, the application suspends by writing the Port Suspend bit (`USB_PRTSUSP`) in the Host Port Control and Status register.

**Footer:**
- "Espressif Systems"
- Page number indicator (1/40)
- Link to submit documentation feedback
- Document version information ("ESP32-S3 TRM (Version 1.7)")