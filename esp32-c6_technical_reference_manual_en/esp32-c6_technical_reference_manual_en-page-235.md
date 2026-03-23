

```markdown
Register 6.101. EFUSE_RD_RS_ERR0_REG (0x01C0)

| Bit | 31 | 30 | 28 | 27 | 26 | 24 | 23 | 22 | 20 | 19 | 18 | 16 | 15 | 14 | 12 | 11 | 10 | 8 | 7 | 6 | 4 | 3 | 2 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|
|     |    | EFUSE_KEY4_FAIL | EFUSE_KEY4_ERR_NUM | EFUSE_KEY3_FAIL | EFUSE_KEY3_ERR_NUM | EFUSE_KEY2_FAIL | EFUSE_KEY2_ERR_NUM | EFUSE_KEY1_FAIL | EFUSE_KEY1_ERR_NUM | EFUSE_KEY0_FAIL | EFUSE_KEY0_ERR_NUM | EFUSE_USR_DATA_FAIL | EFUSE_SYS_PART1_FAIL | EFUSE_MAC_SPI_8M_FAIL | Reset |
| 31  |    | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO |       |

EFUSE_MAC_SPI_8M_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_MAC_SPI_8M_FAIL Represents whether programming MAC_SPI_8M failed.
    O: No failure and the data of MAC_SPI_8M is reliable.
    1: Programming user data failed and the number of error bytes is over 6.
      (RO)

EFUSE_SYS_PART1_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_SYS_PART1_FAIL Represents whether programming system part1 data failed.
    O: No failure and the data of system part1 is reliable.
    1: Programming user data failed and the number of error bytes is over 6.
      (RO)

EFUSE_USR_DATA_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_USR_DATA_FAIL Represents whether programming user data failed.
    O: No failure and the user data is reliable.
    1: Programming user data failed and the number of error bytes is over 6.
      (RO)

EFUSE_KEY0_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_KEY0_FAIL Represents whether programming key0 data failed.
    O: No failure and the data of key0 is reliable.
    1: Programming key0 failed and the number of error bytes is over 6.
      (RO)

EFUSE_KEY1_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_KEY1_FAIL Represents whether programming key1 data failed.
    O: No failure and the data of key1 is reliable.
    1: Programming key1 failed and the number of error bytes is over 6.
      (RO)

EFUSE_KEY2_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_KEY2_FAIL Represents whether programming key2 data failed.
    O: No failure and the data of key2 is reliable.
    1: Programming key2 failed and the number of error bytes is over 6.
      (RO)
```