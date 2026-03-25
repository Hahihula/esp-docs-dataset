

```markdown
Register 5.14. EFUSE_RD_REPEAT_DATA1_REG (0x0034)

| 31 | 28 | 27 | 24 | 23 | 22 | 21 | 20 | 18 | 17 | 16 | 15 |
|-----|----:|:--------------------------|:---------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| 0xO |    |                        | EFUSE_RPT4_RESERVED1_1                         | EFUSE_WDT_DELAY_SEL                                                                                                     |
|     |    |                        | O                                             | Represents whether RTC watchdog timeout threshold is selected at startup. <br> 1: Selected. <br> 0: Not selected (RO) |

EFUSE_SPI_BOOT_CRYPT_CNT Represents whether SPI boot encryption/decryption is enabled.
Odd count of bits with a value of 1: Enabled
Even count of bits with a value of 1: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKEO Represents whether revoking the 1st Secure Boot key is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKE1 Represents whether revoking the 2nd Secure Boot key is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKE2 Represents whether revoking the 3rd Secure Boot key is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_KEY_PURPOSE_O Represents the purpose of Key0. (RO)
EFUSE_KEY_PURPOSE_1 Represents the purpose of Key1. (RO)
```