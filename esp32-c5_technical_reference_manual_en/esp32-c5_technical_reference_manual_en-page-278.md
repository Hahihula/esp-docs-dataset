

```markdown
Chapter 7 eFuse Controller (EFUSE) GoBack

Register 7.7. EFUSE_RD_REPEAT_DATA3_REG (0x003C)

Continued from the previous page...

EFUSE_ENABLE_SECURITY_DOWNLOAD Represents whether security download is enabled. Only downloading into flash is supported. Reading/writing RAM or registers is not supported (i.e. stub download is not supported).
1: Enabled
0: Disabled
(RO)

EFUSE_UART_PRINT_CONTROL Represents the type of UART printing.
0: Force enable printing.
1: Enable printing when GPIO27 is reset at low level.
2: Enable printing when GPIO27 is reset at high level.
3: Force disable printing.
(RO)

EFUSE_FORCE_SEND_RESUME Represents whether ROM code is forced to send a resume command during SPI boot.
1: Forced.
0: Not forced.
(RO)

EFUSE_SECURE_VERSION Represents the security version used by ESP-IDF anti-rollback feature. (RO)

EFUSE_SECURE_BOOT_DISABLED_FAST_WAKE Represents whether FAST VERIFY ON WAKE is disabled when Secure Boot is enabled.
1: Disabled
0: Enabled
(RO)

EFUSE_HYS_EN_PAD Represents whether the hysteresis function of PADO – PAD27 is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_XTS_DPA_PSEUDO_LEVEL Represents the pseudo round level of XTS-AES anti-DPA attack.
0: Disabled
1: Low
2: Moderate
3: High
(RO)

EFUSE_XTS_DPA_CLK_ENABLE Represents whether XTS-AES anti-DPA attack clock is enabled.
0: Disable
1: Enabled
(RO)

EFUSE_ECDSA_P384_ENABLE Represents whether the chip supports ECDSA P384. (RO)
```