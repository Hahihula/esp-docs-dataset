**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.15. EMACCONFIG_REG (0x1000)

**Continuation Notice:**
Continued from the previous page...

**Subsection and Description with Code Example:**
- **Title:** EMACRETRY
  - When this bit is set, the MAC attempts only one transmission. When a collision occurs on the MII interface, the MAC ignores the current frame transmission and reports a Frame Abort with excessive collision error in the transmit frame status. When this bit is reset, the MAC attempts retries based on the settings of the BL field (Bits [6:5]). This bit is applicable only in the half-duplex mode.
  - **Code Example:** EMACPADCRCSTRIp

**Subsection and Description with Code Example:**
- **Title:** EMACPADCRCSTRIp
  - When this bit is set, the MAC strips the Pad or FCS field on the incoming frames only if the value of the length field is less than 1,536 bytes. All received frames with length field greater than or equal to 1,536 bytes are passed to the application without stripping the Pad or FCS field. When this bit is reset, the MAC passes all incoming frames, without modifying them, to the Host.
  - **Code Example:** EMACBACKOFFLIMIT

**Subsection and Description with Code Example:**
- **Title:** EMACBACKOFFLIMIT
  - The Back-Off limit determines the random integer number (r) of slot time delays (512 bit times for 10/100 Mbps) for which the MAC waits before rescheduling a transmission attempt during retries after a collision. This bit is applicable only in the half-duplex mode.
  - **Code Example:** EMACDEFERALCHECK

**Subsection and Description with Code Example:**
- **Title:** EMACDEFERALCHECK
  - Deferral Check (R/W)
    - When this bit is set, the transmit state machine of the MAC is enabled for transmission on the MII. When this bit is reset, the MAC transmits state machine after completion to the current frame and does not receive any further frames.
    - **Code Example:** EMACTX

**Subsection and Description with Code Example:**
- **Title:** EMACTX
  - The receiver state machine of the MAC enables for receiving from MII. When this bit is reset, the MAC receives state machines disabled after completion to reception current frame does not receive any further frames.
  - **Code Example:** EMACRX

**Subsection and Description with Code Example:**
- **Title:** EMACRX
  - These bits control number of preamble bytes that are added beginning every Transmit frame. The preamble reduction occurs only when the MAC is operating in full-duplex mode.

**Footer Information:**
Espressif Systems  
Page Number: 502  
Document Version: ESP32 TRM (Version 5.6)  
Feedback Link Texts:
- Submit Documentation Feedback
- GoBack