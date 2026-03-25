

```markdown
Chapter 7  eFuse Controller (EFUSE)                                                                 GoBack


Register 7.4. EFUSE_RD_REPEAT_DATA0_REG (0x0030)


Continued from the previous page...


EFUSE_WDT_DELAY_SEL Represents RTC watchdog timeout threshold.
    0: The originally configured STGO threshold × 2
    1: The originally configured STGO threshold × 4
    2: The originally configured STGO threshold × 8
    3: The originally configured STGO threshold × 16
        (RO)

EFUSE_BOOTLOADER_ANTI_ROLLBACK_SECURE_VERSION_LO Represents the anti-rollback secure version of the 2nd stage bootloader used by the ROM bootloader (the low part of the field). (RO)
```