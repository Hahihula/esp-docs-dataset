**Title: Chapter 5 eFuse Controller**

**Subtitle: Register 5.99. EFUSE_RD_REPEAT_ERR3_REG (0x188)**

**Table Description:**  
The table lists various error registers in the eFuse controller, each with a specific bit number and description.

| Bit Number | Name | Description |
|------------|------|-------------|
| 31         | EFUSE_DIS_USB_OTG_DOWNLOAD_MODE_ERR | Represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO) |
| 30         | EFUSE_SECURE_VERSION_ERR | Represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO) |
| ...        | ...  | ...          |

**Descriptions of Error Registers:**

- **EFUSE_DIS_USB_OTG_DOWNLOAD_MODE_ERR**: Represents a programming error to corresponding eFuse bit.
- **EFUSE_SECURE_VERSION_ERR**: Represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO)
- **EFUSE_FORCE_SEND_RESUME_ERR**: Represents a programming error to corresponding eFuse bit.

(Note: The list continues with similar descriptions for other registers.)

**Footer:**  
Continued on the next page...

**Company Information:**  
Espressif Systems

**Document Version and Feedback Link:**  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback