**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Section Heading:**
5.5 Registers

**Body Text:**
The addresses in this section are relative to the eFuse Controller base address provided in Table **3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory**.

**Subsection Title:**
Register 5.1. EFUSE_BLK0_RDATA0_REG (0x00)

**Binary Register Diagram Description:**
A binary register diagram is shown with labels for each bit position from the most significant to least significant, ranging from bits `31` down to `0`. The positions are labeled as follows:
- `EFUSE_RD_UART_DOWNLOADDis`
- `EFUSE_RD_FLASH_CRYPTO_CNT`
- `EFUSE_RD_EFUSE_RD_DIS`
- `EFUSE_RD_EFUSE_WR_DIS`

**Field Descriptions:**
- **EFUSE_RD_UART_DOWNLOADDis**: This bit returns the value of `uart_download_dis`. Valid only for ESP32. (RO)
- **EFUSE_RD_FLASH_CRYPTO_CNT**: This field returns the value of flash_crypto_cnt. (RO)
- **EFUSE_RD_EFUSE_RD_DIS**: This field returns the value of efuse_rd_disable. (RO)
- **EFUSE_RD_EFUSE_WR_DIS**: This field returns the value of efuse_wr_disable. (RO)

**Subsection Title:**
Register 5.2. EFUSE_BLK0_RDATA1_REG (0x004)

**Binary Register Diagram Description:**
A binary register diagram is shown with labels for each bit position from the most significant to least significant, ranging from bits `31` down to `0`. The positions are labeled as follows:
- **EFUSE_BLK0_RDATA1_REG**: This field returns the value of the lower 32 bits of WIFI_MAC_Address. (RO)

**Subsection Title:**
Register 5.3. EFUSE_BLK0_RDATA2_REG (0x08)

**Binary Register Diagram Description:**
A binary register diagram is shown with labels for each bit position from the most significant to least significant, ranging from bits `31` down to `0`. The positions are labeled as follows:
- **EFUSE_RD_WIFI_MAC_CRC_HIGH**: This field returns the value of the higher 24 bits of WIFI_MAC_Address. (RO)

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32 TRM (Version 5.6)