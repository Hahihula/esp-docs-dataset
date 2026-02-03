**Chapter Title:**
Chapter 5 eFuse Controller

**Section Header:**
Register 5.13. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

**Table Description and Values:**
- The table lists various registers with their descriptions, bit positions in the register, data types, default values when reset, possible states, description of each state.
  
| Bit Position | Register Name | Data Type | Default Value When Reset | Possible States |
|--------------|---------------|-----------|--------------------------|------------------|
| 31           | (reserved)    | -         | -                        | -                |
| ...          | EFUSE_RD_DIS | Boolean   | 0: Disabled. 1: Enabled. (RO) | -               |
| ...          | EFUSE_RPT4_RESERVED3 | Reserved (used for four backups method). (RO) | -                 | -              |
| ...          | EFUSE_DIS_ICACHE | Boolean   | 0: Disabled. 1: Enabled. (RO) | -                |
| ...          | EFUSE_DIS_DCACHE | Boolean   | 0: Disabled. 1: Enabled. (RO) | -               |
| ...          | EFUSE_DIS_DOWNLOAD_ICACHE | Boolean   | 0: Disabled. 1: Enabled. (RO) | -                 |
| ...          | EFUSE_DIS_DOWNLOAD_DCACHE | Boolean   | 0: Disabled. 1: Enabled. (RO) | -                |
| ...          | EFUSE_DIS_FORCE_DOWNLOAD | Boolean   | 0: Disabled. 1: Enabled. (RO) | -               |
| ...          | EFUSE_DIS_USB_OTG | Boolean   | 0: Enabled. 1: Disabled. (RO) | -                 |
| ...          | EFUSE_DIS_TWAI | Boolean   | 0: Disabled. 1: Enabled. (RO) | -                |
| ...          | EFUSE_DIS_APP_CPU | Boolean   | 0: Disabled. 1: Enabled. (RO) | -               |
| ...          | EFUSE_SOFDis_JTAG | Boolean   | 0: Disabled. Users can re-enable JTAG by HMAC module again. Even number of 1: Enabled. (RO) | -                 |
| ...          | EFUSE_DIS_PAD_TJAG | Boolean   | 0: Enabled. (RO) | -                |
| ...          | EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT | Boolean   | 0: Disabled. 1: Enabled. (RO) | -               |

**Footer Note:** 
Continued on the next page...

**Document Footer Information:**
Espressif Systems
431 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback