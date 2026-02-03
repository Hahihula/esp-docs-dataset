**Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Link:**
GoBack

**Register Information:**
- Register Number: 34.29.
- Register Name: SDHOST_RST_N_REG (0x0078)
- Bit Positions and Values:
  - [31] 
  - [2]
  - [1]
  - [0]

**Bit Description Table:**
- **SDHOST_RST_CARD_RESET Hardware reset.**
  - `1`: Active mode;
  - `0`: Reset.
  
  These bits cause the cards to enter pre-idle state, which requires them to be re-initialized. SD-HOST_RST_CARD_RESET[0] should be set to '1'b0 to reset card0; SDHOST_RST_CARD_RESET[1] should be set to '1'b0 to reset card1. (R/W)

**Footer:**
- Company Name: Espressif Systems
- Document Version and Type Information:
  - Page Number: 1301
  - Document Title: ESP32-S3 TRM (Version 1.7)
  - Link for Submitting Documentation Feedback