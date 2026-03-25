

```markdown
Chapter 5 eFuse Controller (EFUSE)
GoBack

Register 5.6. EFUSE_RD_REPEAT_DATA2_REG (0x0038)

Continued from the previous page...

EFUSE_FORCE_SEND_RESUME Represents whether ROM code is forced to send a resume command during SPI boot.
1: Forced.
O: Not forced.
(RO)

EFUSE_SECURE_VERSION Represents the security version used by ESP-IDF anti-rollback feature.
(RO)

EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE Represents whether FAST_VERIFY_ON_WAKE is disabled when Secure Boot is enabled.
1: Disabled
O: Enabled
(RO)

EFUSE_HYS_EN_PAD Represents whether the hysteresis function of corresponding PAD is enabled.
1: Enabled
O: Disabled
(RO)

EFUSE_XTS_DPA_CLK_ENABLE Represents whether anti-DPA attack clock function is enabled.
1: Enabled
O: Disabled
(RO)

EFUSE_XTS_DPA_PSEUDO_LEVEL Represents the anti-SCA attack pseudo function level.
3: High
2: Moderate
1: Low
O: Decided by register configuration
(RO)

EFUSE_DIS_WIFI6 Represents whether the Wi-Fi 6 feature is enabled.
1: Disabled
O: Enabled
(RO)

EFUSE_ECDSA_DISABLE_P192 Represents whether to disable P192 curve in ECDSA.
1: Disabled
O: Enabled
(RO)

Continued on the next page...
```