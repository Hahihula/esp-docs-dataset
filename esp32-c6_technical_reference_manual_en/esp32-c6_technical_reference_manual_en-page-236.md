
```markdown
Chapter 6 eFuse Controller

Register 6.101. EFUSE_RD_RS_ERR0_REG (0x01C0)

Continued from the previous page...

EFUSE_KEY3_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_KEY3_FAIL Represents whether programming key3 data failed.
O: No failure and the data of key3 is reliable.
1: Programming key3 failed and the number of error bytes is over 6.
(RO)

EFUSE_KEY4_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_KEY4_FAIL Represents whether programming key4 data failed.
O: No failure and the data of key4 is reliable.
1: Programming key4 failed and the number of error bytes is over 6.
(RO)

Register 6.102. EFUSE_RD_RS_ERR1_REG (0x01C4)

EFUSE_KEY5_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_KEY5_FAIL Represents whether programming key5 data failed.
O: No failure and the data of key5 is reliable.
1: Programming key5 failed and the number of error bytes is over 6.
(RO)

EFUSE_SYS_PART2_ERR_NUM Represents the number of error bytes. (RO)

EFUSE_SYS_PART2_FAIL Represents whether programming system part2 data failed.
O: No failure and the data of system part2 is reliable.
1: Programming user data failed and the number of error bytes is over 6.
(RO)
```