**Title: Chapter 5 eFuse Controller**

---

### Register 5.101. EFUSE_RD_RS_ERRO_REG (0x10CO)

| Bit | Description |
|-----|-------------|
| 3   | EFUSE_KEY4_FAIL |
| 2   | EFUSE_KEY4_ERR_NUM |
| ... | ... |
| 6   | EFUSE_USER_DATA_FAIL |
| 5   | EFUSE_SYS_PART1_FAIL |
| 4   | EFUSE_USR_DATA_ERRNUM |
| 3   | EFUSE_KEYO_ERR_NUM |
| 2   | EFUSE_KEYO_FAIL |
| 1   | EFUSE_KEY1_ERR_NUM |
| ... | ... |

**EFUSE_MAC_SPI_8M_ERR_NUM**: Represents the number of error bytes during programming MAC_SPI_8M. (RO)

**EFUSE_MAC_SPI_8M_FAIL**: Represents whether or not the data is reliable. O: Means no failure and that the data of MAC_SPI_8M is reliable. 1: Means that programming data of MAC_SPI_8M has failed and the number of error bytes is over 6. (RO)

**EFUSE_SYS_PART1_NUM**: Represents the number of error bytes during programming system part1. (RO)

**EFUSE_SYS_PART1_FAIL**: Represents whether or not the data is reliable. O: Means no failure and that the data of system part1 is reliable. 1: Means that programming data of system part1 failed and the number of error bytes is over 6. (RO)

**EFUSE_USR_DATA_ERRNUM**: Represents the number of error bytes during programming user data. (RO)

**EFUSE_USR_DATA_FAIL**: Represents whether or not the data is reliable. O: Means no failure and that the user data is reliable. 1: Means that programming user data failed and the number of error bytes is over 6. (RO)

**EFUSE_KEYO_ERR_NUM**: Represents the number of error bytes during programming KEYO. (RO)

**EFUSE_KEYO_FAIL**: Represents whether or not the data is reliable. O: Means no failure and that the data of key0 is reliable. 1: Means that programming key0 failed and the number of error bytes is over 6. (RO)

**EFUSE_KEY1_ERR_NUM**: Represents the number of error bytes during programming KEY1. (RO)

**EFUSE_KEY1_FAIL**: Represents whether or not the data is reliable. O: Means no failure and that the data of key1 is reliable. 1: Means that programming key1 failed and the number of error bytes is over 6. (RO)

**EFUSE_KEY2_ERR_NUM**: Represents the number of error bytes during programming KEY2. (RO)

**EFUSE_KEY2_FAIL**: Represents whether or not the data is reliable. O: Means no failure and that the data of key2 is reliable. 1: Means that programming key2 failed and the number of error bytes is over 6. (RO)

---

Continued on the next page...

---

*Espressif Systems*
464
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)