

```markdown
Chapter 5 eFuse Controller (EFUSE)

Register 5.30. EFUSE_RD_RS_DATA_ERR1_REG (0x0194)
```

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 8   | EFUSE_RD_SYS_PART2_DATA_FAIL |
| 7   | EFUSE_RD_KEY5_DATA_ERR_NUM |
| 6   | EFUSE_RD_SYS_PART2_DATA_FAIL |
| 4   | EFUSE_RD_KEY5_DATA_FAIL |
| 3   | EFUSE_RD_KEY5_DATA_ERR_NUM |
| 2   | Reset       |

EFUSE_RD_KEY5_DATA_ERR_NUM Represents the number of error bytes in RD_KEY5_DATA. (RO)

EFUSE_RD_KEY5_DATA_FAIL Represents error status of register.
0: No failure and that the data of RD_KEY5_DATA is reliable.
1: Programming RD_KEY5_DATA failed and the number of error bytes is over 6. (RO)

EFUSE_RD_SYS_PART2_DATA_ERR_NUM Represents the number of error bytes in RD_SYS_PART2_DATA. (RO)

EFUSE_RD_SYS_PART2_DATA_FAIL Represents error status of register.
0: No failure and that the data of RD_SYS_PART2_DATA is reliable.
1: Programming RD_SYS_PART2_DATA failed and the number of error bytes is over 6. (RO)

Register 5.31. EFUSE_DATE_REG (0x0198)
```

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 28  | EFUSE_DATE  |
| 27  |             |
|     | 0x2401100   |

EFUSE_DATE Stores eFuse version. (R/W)
```