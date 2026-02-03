**Title: Chapter 5 eFuse Controller**

**Subtitle: Register 5.97. EFUSE_RD_REPEAT_ERR1_REG (0x180)**

**Table Description:**  
The table lists various error registers in the eFuse controller, each with a specific bit number and description.

- **EFUSE_KEY_PURPOSE_1_ERR**
- **EFUSE_SECURE_BOOT_KEY_REVOKE2_ERR**
- **EFUSE_SPI_BOOT_CRYPT_CNT_ERR**
- **EFUSE_WDT_DELAY_SEL_ERR**

**Bit Positions:**
- EFUSE_VDD_SPI_XPD_ERR
- EFUSE_VDD_SPI_TIEH_ERR
- EFUSE_VDD_SPI_FORCE_ERR

**Descriptions for each bit position (in hexadecimal format):**
- 0x0 to 0x18, with specific bits labeled from left to right.

**Error Descriptions:**

- **EFUSE_VDD_SPI_XPD_ERR:** Represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO)
- **EFUSE_VDD_SPI_TIEH_ERR:** Represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO)
- **EFUSE_VDD_SPI_FORCE_ERR:** Represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO)
- **EFUSE_WDT_DELAY_SEL_ERR:** Represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO)

**Additional Error Descriptions:**

- **EFUSE_SPI_BOOT_CRYPT_CNT_ERR**
- **EFUSE_SECURE_BOOT_KEY_REVOKE0_ERR**
- **EFUSE_SECURE_BOOT_KEY_REVOKE1_ERR**
- **EFUSE_SECURE_BOOT_KEY_REVOKE2_ERR**

Each of these represents a programming error to corresponding eFuse bit if any bit in this field is 1. (RO)

**Footer:**
Espressif Systems  
460 ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)