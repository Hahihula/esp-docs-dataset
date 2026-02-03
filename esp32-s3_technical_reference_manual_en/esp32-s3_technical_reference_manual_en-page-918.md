**Title: Chapter 23 External Memory Encryption and Decryption (XTS_AES)**

---

### Register 23.8. XTS_AES_STATE_REG (0x0058)

| Field | Description |
|-------|-------------|
| **XTS_AES_STATE** | Indicates the status of the Manual Encryption block. (RO) |
| - `0x0` (XTS_AES_IDLE): idle; |
| - `0x1` (XTS_AES BUSY): busy with encryption; |
| - `0x2` (XTS_AES DONE): encryption is completed, but the encrypted result is not accessible to SPI; |
| - `0x3` (XTS_AES RELEASE): encrypted result is accessible to SPI. |

---

### Register 23.9. XTS_AES_DATE_REG (0x005C)

| Field | Description |
|-------|-------------|
| **XTS_AES_DATE** | Version control register. (R/W) |

---

*Espressif Systems*
*ESP32-S3 TRM (Version 1.7)*

[Submit Documentation Feedback](#)