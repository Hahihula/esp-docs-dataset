**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Navigation Link:**
GoBack

**Section Heading:**
Register 24.20. EMACDEBUG_REG (0x1024)

**Continuation Note:**
Continued from the previous page...

**Field Descriptions and Values in Table Format:**

- **MTLRFRCS**: This field gives the state of the Rx FIFO read Controller:
  - `2'b00`: IDLE state.
  - `2'b01`: Reading frame data.
  - `2'b10`: Reserved.

- **MTLRFWCAS**: When high, this bit indicates that the MTL Rx FIFO Write Controller is active and is transferring a received frame to the FIFO. (RO)

- **MACRFFCS**: When high, this field indicates the active state of the FIFO Read and Write controllers of the MAC Receive Frame Controller Module. MACRFFCS[1] represents the status of FIFO Read controller. MACRFFCS[0] represents the status of small FIFO Write controller. (RO)

- **MACRPES**: When high, this bit indicates that the MAC MII receive protocol engine is actively receiving data and not in IDLE state. (RO)

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version Note at Bottom Right Corner:**
ESP32 TRM (Version 5.6)