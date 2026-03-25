

```markdown
Chapter 5 eFuse Controller (EFUSE)
GoBack

Register 5.29. EFUSE_RD_RS_DATA_ERR0_REG (0x0190)

Continued from the previous page...

EFUSE_RD_KEY2_DATA_FAIL Represents error status of register.
    0: No failure and the data of RD_KEY2_DATA is reliable.
    1: Programming RD_KEY2_DATA failed and the number of error bytes is over 6.
        (RO)

EFUSE_RD_KEY3_DATA_ERR_NUM Represents the number of error bytes in RD_KEY3_DATA. (RO)

EFUSE_RD_KEY3_DATA_FAIL Represents error status of register.
    0: No failure and the data of RD_KEY3_DATA is reliable.
    1: Programming RD_KEY3_DATA failed and the number of error bytes is over 6.
        (RO)

EFUSE_RD_KEY4_DATA_ERR_NUM Represents the number of error bytes in RD_KEY4_DATA. (RO)

EFUSE_RD_KEY4_DATA_FAIL Represents error status of register.
    0: No failure and the data of RD_KEY4_DATA is reliable.
    1: Programming RD_KEY4_DATA failed and the number of error bytes is over 6.
        (RO)
```