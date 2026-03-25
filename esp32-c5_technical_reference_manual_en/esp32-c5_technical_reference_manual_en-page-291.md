

```markdown
Chapter 7 eFuse Controller (EFUSE) GoBack

Register 7.29. EFUSE_RD_RS_DATA_ERR0_REG (0x0190)

Continued from the previous page...

EFUSE_RD_KEY2_DATA_FAIL Represents whether programming key2 data failed.
O: No failure and the data of RD_KEY2_DATA is reliable.
1: Programming RD_KEY2_DATA failed and the number of error bytes is over 6.
(RO)

EFUSE_RD_KEY3_DATA_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_RD_KEY3_DATA_FAIL Represents whether programming key3 data failed.
O: No failure and the data of RD_KEY3_DATA is reliable.
1: Programming RD_KEY3_DATA failed and the number of error bytes is over 6.
(RO)

EFUSE_RD_KEY4_DATA_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_RD_KEY4_DATA_FAIL Represents whether programming key4 data failed.
O: No failure and the data ofRD_KEY4_DATA is reliable.
1: Programming RD_KEY4_DATA failed and the number of error bytes is over 6.
(RO)
```