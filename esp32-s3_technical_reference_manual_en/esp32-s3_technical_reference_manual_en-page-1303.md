**Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Link:**
GoBack

**Register Information:**
- **Register Number:** Register 34.32.
- **Register Name:** SDHOST_DBADDR_REG (0x0088)
- **Address:** 0x00000000
- **Reset Value:** 

**Description of the Register:**
SDHOST_DBADDR_REG - Start of Descriptor List.

Contains the base address of the First Descriptor.
The LSB bits [1:0] are ignored and taken as all-zero by the IDMAC internally. Hence these LSB bits may be treated as read-only. (R/W)

**Footer Information:**
- **Company:** Espressif Systems
- **Page Number:** 1303
- **Document Title:** ESP32-S3 TRM (Version 1.7)
- **Link:** Submit Documentation Feedback