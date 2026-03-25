

```markdown
Register 5.101. EFUSE_RD_RS_ERRRO_REG (0x01CO)
```

| 31 | 30 | 28 | 27 | 26 | 24 | 23 | 22 | 20 | 19 | 18 | 16 | 15 | 14 | 12 | 11 | 10 | 8 | 7 | 6 | 4 | 3 | 2 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0  | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | 0xO | 0   | Reset |

EFUSE_MAC_SYS_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_MAC_SYS_FAIL Represents whether programming MAC_SYS failed.
O: No failure and the data of MAC_SYS is reliable.
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