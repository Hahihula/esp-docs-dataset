

```markdown
Chapter 5 eFuse Controller (EFUSE) GoBack


Register 5.5. EFUSE_RD_REPEAT_DATA1_REG (0x0034)

| Bit | 31 | 28 | 27 | 26 | 25 | 24 | 23 | 20 | 19 | 16 | 15 | 12 | 11 | 8 | 7 | 4 | 3 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |
| Value | 0x0 | 0 | 0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 |

EFUSE_KEY_PURPOSE_0 Represents the purpose of Key0. (RO)

EFUSE_KEY_PURPOSE_1 Represents the purpose of Key1. (RO)

EFUSE_KEY_PURPOSE_2 Represents the purpose of Key2. (RO)

EFUSE_KEY_PURPOSE_3 Represents the purpose of Key3. (RO)

EFUSE_KEY_PURPOSE_4 Represents the purpose of Key4. (RO)

EFUSE_KEY_PURPOSE_5 Represents the purpose of Key5. (RO)

EFUSE_SEC_DPA_LEVEL Represents whether to determine DPA secure level by configuring the clock random frequency dividing mode.
0: No effect
1: Determine
(RO)

EFUSE_SECURE_BOOT_EN Represents whether Secure Boot is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE Represents whether aggressive revocation of Secure Boot is enabled.
1: Enabled.
0: Disabled
(RO)

EFUSE_FLASH_TPUW Represents the flash waiting time after power-up, in unit of ms. When the value less than 15, the waiting time is the programmed value. Otherwise, the waiting time is 2 times the programmed value. (RO)
```