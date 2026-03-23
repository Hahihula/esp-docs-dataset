

```markdown
Chapter 6 eFuse Controller

Register 6.16. EFUSE_RD_REPEAT_DATA3_REG (0x003C)

Continued from the previous page...

EFUSE_UART_PRINT_CONTROL Represents the type of UART printing.
- 0: Force enable printing.
- 1: Enable printing when GPIO8 is reset at low level.
- 2: Enable printing when GPIO8 is reset at high level.
- 3: Force disable printing.
(RO)

EFUSE_RPT4_RESERVED3_4 Reserved. (RO)
EFUSE_RPT4_RESERVED3_3 Reserved. (RO)
EFUSE_RPT4_RESERVED3_2 Reserved. (RO)
EFUSE_RPT4_RESERVED3_1 Reserved. (RO)

EFUSE_FORCE_SEND_RESUME Represents whether ROM code is forced to send a resume command during SPI boot.
- 1: Forced.
- 0: Not forced.
(RO)

EFUSE_SECURE_VERSION Represents the security version used by ESP-IDF anti-rollback feature.
(RO)

EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE Represents whether FAST VERIFY ON WAKE is disabled when Secure Boot is enabled.
- 1: Disabled
- 0: Enabled
(RO)

EFUSE_RPT4_RESERVED3_0 Reserved. (RO)
```

```markdown
Register 6.17. EFUSE_RD_REPEAT_DATA4_REG (0x0040)

| 31 | 24 | 23 | ... | 0 |
|----|----|----|-----|---|
|    |    |    |     |   |
| 0x0 |    |    | 0x0000 | Reset |

EFUSE_RPT4_RESERVED4_1 Reserved. (RO)
EFUSE_RPT4_RESERVED4_0 Reserved. (RO)
```