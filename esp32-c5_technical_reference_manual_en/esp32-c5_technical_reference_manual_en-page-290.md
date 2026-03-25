

```markdown
Register 7.29. EFUSE_RD_RS_DATA_ERR_REG (0x0190)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | EFUSE_RD_KEY4_DATA_FAIL             |                                                                             |
| 30  | EFUSE_RD_KEY4_DATA_ERR_NUM          | Represents the number of error bytes. (RO)                                  |
| 27  | EFUSE_RD_KEY3_DATA_FAIL             |                                                                             |
| 26  | EFUSE_RD_KEY3_DATA_ERR_NUM          |                                                                             |
| 24  | EFUSE_RD_KEY2_DATA_FAIL             |                                                                             |
| 23  | EFUSE_RD_KEY2_DATA_ERR_NUM          |                                                                             |
| 20  | EFUSE_RD_KEY1_DATA_FAIL             |                                                                             |
| 19  | EFUSE_RD_KEY1_DATA_ERR_NUM          |                                                                             |
| 18  | EFUSE_RD_KEY0_DATA_FAIL             |                                                                             |
| 17  | EFUSE_RD_KEY0_DATA_ERR_NUM          |                                                                             |
| 16  | EFUSE_RD_USR_DATA_FAIL              |                                                                             |
| 15  | EFUSE_RD_USR_DATA_ERR_NUM           | Represents the number of error bytes. (RO)                                  |
| 14  | EFUSE_RD_SYS_PART1_DATA_FAIL        | Represents whether programming system part1 data failed.                    |
| 13  | EFUSE_RD_SYS_PART1_DATA_ERR_NUM     | Represents the number of error bytes. (RO)                                  |
| 12  | EFUSE_RD_KEYO_DATA_FAIL             |                                                                             |
| 11  | EFUSE_RD_KEYO_DATA_ERR_NUM          | Represents the number of error bytes. (RO)                                  |
| 10  | EFUSE_RD_KEY1_DATA_FAIL             |                                                                             |
| 9   | EFUSE_RD_KEY1_DATA_ERR_NUM          | Represents whether programming key1 data failed.                            |
| 8   | EFUSE_RD_KEY2_DATA_FAIL             |                                                                             |
| 7   | EFUSE_RD_KEY2_DATA_ERR_NUM          | Represents the number of error bytes. (RO)                                  |
| 6   | EFUSE_RD_MAC_SYS_FAIL               | Represents whether programming RD_MAC_SYS failed.                           |
| 5   | EFUSE_RD_MAC_SYS_ERR_NUM            | Represents the number of error bytes. (RO)                                  |
| 4   | EFUSE_RD_USR_DATA_ERR_NUM           |                                                                             |
| 3   | EFUSE_RD_SYS_PART1_DATA_ERR_NUM     |                                                                             |
| 2   | EFUSE_RD_KEYO_DATA_ERR_NUM          |                                                                             |
| 1   | EFUSE_RD_KEY1_DATA_ERR_NUM          |                                                                             |
| 0   | Reset                               |                                                                             |

EFUSE_RD_MAC_SYS_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_RD_MAC_SYS_FAIL Represents whether programming RD_MAC_SYS failed.
O: No failure and the data of RD_MAC_SYS is reliable.
1: Programming user data failed and the number of error bytes is over 6. (RO)

EFUSE_RD_SYS_PART1_DATA_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_RD_SYS_PART1_DATA_FAIL Represents whether programming system part1 data failed.
O: No failure and the data of RD_SYS_PART1_DATA is reliable.
1: Programming user data RD_SYS_PART1_DATA failed and the number of error bytes is over 6. (RO)

EFUSE_RD_USR_DATA_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_RD_USR_DATA_FAIL Represents whether programming user data failed.
O: No failure and the user data is reliable.
1: Programming user data failed and the number of error bytes is over 6. (RO)

EFUSE_RD_KEYO_DATA_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_RD_KEYO_DATA_FAIL Represents whether programming key0 data failed.
O: No failure and the data of RD_KEYO_DATA is reliable.
1: Programming RD_KEYO_DATA failed and the number of error bytes is over 6. (RO)

EFUSE_RD_KEY1_DATA_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_RD_KEY1_DATA_FAIL Represents whether programming key1 data failed.
O: No failure and the data of RD_KEY1_DATA is reliable.
1: Programming RD_KEY1_DATA failed and the number of error bytes is over 6. (RO)

EFUSE_RD_KEY2_DATA_ERR_NUM Represents the number of error bytes. (RO)
```