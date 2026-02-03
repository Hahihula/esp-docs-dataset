**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**GoBack Link:** GoBack

---

### Register Descriptions:

#### Register 12.3:
- **Name:** TIMG_TxHI_REG (X: 0-1) (0x0008+0x24*x)
- **Description:** After writing to TIMG_TxUPDATE_REG, the high 22 bits of the time-base counter of timer x can be read here. (RO)

#### Register 12.4:
- **Name:** TIMG_TxUPDATE_REG (X: 0-1) (0x000C+0x24*x)
- **Description:** After writing 0 or 1 to TIMG_TxUPDATE_REG, the counter value is latched.
- **Access Mode:** (R/W/SC)

#### Register 12.5:
- **Name:** TIMG_TxALARMLO_REG (X: 0-1) (0x001C+0x24*x)
- **Description:** Timer x alarm trigger time-base counter value, low 32 bits.
- **Access Mode:** (R/W)

#### Register 12.6:
- **Name:** TIMG_TxALARMHI_REG (X: 0-1) (0x0014+0x24*x)
- **Description:** Timer x alarm trigger time-base counter value, high 22 bits.
- **Access Mode:** (R/W)

---

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)