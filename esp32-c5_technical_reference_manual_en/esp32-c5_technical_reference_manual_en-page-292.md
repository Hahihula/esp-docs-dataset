

```markdown
Chapter 7 eFuse Controller (EFUSE)                                                                 GoBack

Register 7.30. EFUSE_RD_RS_DATA_ERR1_REG (0x0194)

EFUSE_RD_KEY5_DATA_ERR_NUM   Represents the number of error bytes in RD_KEY5_DATA. (RO)

EFUSE_RD_KEY5_DATA_FAIL      Represents whether programming key5 data failed.
    0: No failure and the data of RD_KEY5_DATA is reliable.
    1: Programming RD_KEY5_DATA failed and the number of error bytes is over 6.
    (RO)

EFUSE_RD_SYS_PART2_DATA_ERR_NUM   Represents the number of error bytes. (RO)

EFUSE_RD_SYS_PART2_DATA_FAIL      Represents whether programming system part2 data failed.
    0: No failure and the data of RD_SYS_PART2_DATA is reliable.
    1: Programming RD_SYS_PART2_DATA failed and the number of error bytes is over 6.
    (RO)

Register 7.31. EFUSE_DATE_REG (0x0198)

EFUSE_DATE   Version control register. (R/W)
```