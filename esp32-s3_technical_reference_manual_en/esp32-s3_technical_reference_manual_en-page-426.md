**Title: Chapter 5 eFuse Controller**

**GoBack**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Interrupt Register** |                 |         |        |
| EFUSE_INT_RAW_REG | eFuse raw interrupt register | 0x01D8 | R/WC/SS |
| EFUSE_INT_ST_REG | eFuse interrupt status register | 0x01DC | RO |
| EFUSE_INT_ENA_REG | eFuse interrupt enable register | 0x01E0 | RW |
| EFUSE_INT_CLR_REG | eFuse interrupt clear register | 0x01E4 | WO |
| **Version Register** |                 |         |        |
| EFUSE_DATE_REG | Version control register | 0x01FC | R/W |

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)