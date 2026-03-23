

```markdown
Register 4.101. EFUSE_RD_RS_ERRRO_REG (0x01CO)

| Bit | 31 | 30 | 28 | 27 | 26 | 24 | 23 | 22 | 20 | 19 | 18 | 16 | 15 | 14 | 12 | 11 | 10 | 8 | 7 | 6 | 4 | 3 | 2 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|
|     |    | EFUSE_KEY3_FAIL | EFUSE_KEY4_ERR_NUM | EFUSE_KEY2_FAIL | EFUSE_KEY3_ERR_NUM | EFUSE_KEY1_FAIL | EFUSE_KEY0_ERR_NUM | EFUSE_KEY1_ERR_NUM | (reserved) | EFUSE_SYS_PART1_FAIL | EFUSE_MAC_SPI_8M_FAIL | EFUSE_USR_DATA_ERR_NUM | EFUSE_SYS_PART1_NUM | Reset |
| Value | 0xO | 0 | 0xO | 0 | 0xO | 0 | 0xO | 0 | 0xO | 0 | 0xO | 0 | 0xO |

EFUSE_MAC_SPI_8M_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_SYS_PART1_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_MAC_SPI_8M_FAIL O: Means no failure and that the data of MAC_SPI_8M is reliable 1:
Means that programming data of MAC_SPI_8M failed and the number of error bytes is over 6.
(RO)

EFUSE_USR_DATA_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_SYS_PART1_FAIL O: Means no failure and that the data of system part1 is reliable 1:
Means that programming data of system part1 failed and the number of error bytes is over 6.
(RO)

EFUSE_KEYO_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_USR_DATA_FAIL O: Means no failure and that the user data is reliable 1:
Means that programming user data failed and the number of error bytes is over 6. (RO)

EFUSE_KEY1_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_KEYO_FAIL O: Means no failure and that the data of key0 is reliable 1:
Means that programming key0 failed and the number of error bytes is over 6. (RO)

EFUSE_KEY2_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_KEY1_FAIL O: Means no failure and that the data of key1 is reliable 1:
Means that programming key1 failed and the number of error bytes is over 6. (RO)

EFUSE_KEY3_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_KEY2_FAIL O: Means no failure and that the data of key2 is reliable 1:
Means that programming key2 failed and the number of error bytes is over 6. (RO)

EFUSE_KEY4_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_KEY3_FAIL O: Means no failure and that the data of key3 is reliable 1:
Means that programming key3 failed and the number of error bytes is over 6. (RO)
```