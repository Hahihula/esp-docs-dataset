**Title: Chapter 5 eFuse Controller**

---

**Register 5.99. EFUSE_RD_REPEAT_ERR3_REG (0x188)**

Continued from the previous page...

- **EFUSE_SECURE_VERSION_ERR**
  - Represents a programming error to corresponding eFuse bit if any bit in this field is 1.
  
- **EFUSE_DIS_USB_OTG_DOWNLOAD_MODE_ERR**
  - Represents a programming error to corresponding eFuse bit if any bit in this field is 1.

---

**Register 5.100. EFUSE_RD_REPEAT_ERR4_REG (0x18C)**

| Bit | Description |
|-----|-------------|
| 31-24 | Reserved |
| 23   | EFUSE_RPT4_ERR |
| 22   | EFUSE_RPT4_RESERVED2_ERR |
| 21-0  | Reset |

EFUSE_RPT4_RESERVED2_ERR
- Represents a programming error to corresponding eFuse bit if any bit in this field is 1.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)