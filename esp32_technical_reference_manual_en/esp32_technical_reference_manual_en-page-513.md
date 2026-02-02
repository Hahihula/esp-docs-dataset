**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Titles and Register Descriptions with Details:**

1. **Register Description for EMACPLITIMERSCONTROL_REG (0x1034):**
   - **LPI_LS_TIMER:** This field specifies the minimum time in milliseconds for which the link status from the PHY should be up (OKAY) before the LPI pattern can be transmitted to the PHY. The MAC does not transmit the LPI pattern even when the LIEN bit is set unless the LPI_LS_Timer reaches the programmed terminal count. The default value of the LPI_LS_Timer is 1000 (1 sec) as defined in the IEEE standard.(R/W)
   - **LPI_TW_TIMER:** This field specifies the minimum time in microseconds for which the MAC waits after it stops transmitting the LPI pattern to the PHY and before it resumes the normal transmission. The TLPIEX status bit is set after the expiry of this timer.(R/W)

2. **Register Description for EMACINTS_REG (0x1038):**
   - **LPIINTS:** When the Energy Efficient Ethernet feature is enabled, this bit is set for any LPI state entry or exit in the MAC Transmitter or Receiver. This bit is cleared on reading Bit[0] of Register (LPI Control and Status Register). (RO)
   - **PMTINTS:** This bit is set when a magic packet or remote wake-up frame is received in the power-down mode (see Bit[5] and Bit[6] in the PMT Control and Status Register). This bit is cleared when both Bits[6:5] are cleared because of a read operation to the PMT Control and Status register. This bit is valid only when you select the optional PMT module during core configuration.(RO)

**Footer Information:**
- Page number 513
- Company name: Espressif Systems
- Document version information: ESP32 TRM (Version 5.6)
- Link for submitting documentation feedback

**Navigation Links:**
- GoBack button at the top right corner of each section.

**Visual Elements Description:** 
- Each register description is accompanied by a binary representation diagram showing bit positions and their corresponding labels.
- The diagrams are structured with lines indicating bits, numbers representing specific locations within registers (e.g., 31 to 0), letters for reserved or special functions like "LPI" followed by an underscore and the function name.