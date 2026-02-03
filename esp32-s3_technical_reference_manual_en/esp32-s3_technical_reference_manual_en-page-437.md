**Title: Chapter 5 eFuse Controller**

---

### Register 5.20. EFUSE_RD_MAC_SPI_SYS_2_REG (0x004C)

- **EFUSE_SPI_PAD_CONF_1**: Represents the second part of SPI_PAD_CONF. (RO)
  
  - **Value:** `0x000000`
  - **Reset Value:** `0`

---

### Register 5.21. EFUSE_RD_MAC_SPI_SYS_3_REG (0x0050)

- **EFUSE_DATA_PARTO_0**: Represents the bits O~7 of the first part of system data. (RO)
  
  - **Value Diagram:**
    ```
    31   24   23   22   21   20   19   18   17
    0xO   OXO   OXO   OXO   OXO   OXO   OXO   OXOO
    ```
  
- **EFUSE_SPI_PAD_CONF_2**: Represents the second part of SPI_PAD_CONF. (RO)
  
- **EFUSE_WAVER_VERSION**: Represents wafer version information. (RO)
  
- **EFUSE_PKG_VERSION**: Represents package version information. (RO)
  
- **EFUSE_DATA_PARTO_1**: Represents the bits 8~39 of the first part of system data. (RO)

---

### Register 5.22. EFUSE_RD_MAC_SPI_SYS_4_REG (0x0054)

- **EFUSE_DATA_PARTO_1**: Represents the bits 8~39 of the first part of system data. (RO)
  
  - **Value:** `0x000000`
  - **Reset Value:** `0`

---

**Footer:**
Espressif Systems
437 ESP32-S3 TRM (Version 1.7)

Submit Documentation Feedback