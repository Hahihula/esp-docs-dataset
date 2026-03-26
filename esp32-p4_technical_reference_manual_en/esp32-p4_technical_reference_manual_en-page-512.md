

```markdown
Chapter 8 eFuse Controller (EFUSE) GoBack

Register 8.7. EFUSE_RD_REPEAT_DATA3_REG (0x003C)

Continued from the previous page...

EFUSE_UART_PRINT_CONTROL Represents the type of UART printing.
- O: Force enable printing.
- 1: Enable printing when GPIO36 is reset at low level.
- 2: Enable printing when GPIO36 is reset at high level.
- 3: Force disable printing.
(RO)

EFUSE_FORCE_SEND_RESUME Represents whether ROM code is forced to send a resume command during SPI boot.
- 1: Forced.
- O: Not forced.
(RO)

EFUSE_SECURE_VERSION Represents the security version used by ESP-IDF anti-rollback feature.
(RO)

EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE Represents whether FAST VERIFY ON WAKE is disabled when Secure Boot is enabled.
- 1: Disabled
- O: Enabled
(RO)

EFUSE_HYS_EN_PAD Represents whether the hysteresis function of PADO – PAD27 is enabled.
- 1: Enabled
- O: Disabled
(RO)

EFUSE_DCDC_VSET Represents the default DCDC voltage. (RO)
```