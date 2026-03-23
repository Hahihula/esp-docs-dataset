

```markdown
| 31 | 28 | 27 | 24 | 23 | 22 | 21 | 20 | 18 | 17 | 16 | 15 |
|-----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| OxO |    |    |   O |   O |   O | OxO | OxO |    |    |    |
|     |    |    |     |     |     |     |     |     |     | Reset |
```

EFUSE_RPT4_RESERVED1_0 Reserved. (RO)

EFUSE_WDT_DELAY_SEL Represents whether RTC watchdog timeout threshold is selected at startup.

1: Selected.
O: Not selected
(RO)

EFUSE_SPI_BOOT_CRYPT_CNT Represents whether SPI boot encryption/decryption is enabled.

Odd count of bits with a value of 1: Enabled

Even count of bits with a value of 1: Disabled

(RO)

EFUSE_SECURE_BOOT_KEY_REVOKEO Represents whether revoking the first Secure Boot key is enabled.

1: Enabled
O: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKE1 Represents whether revoking the second Secure Boot key is enabled.

1: Enabled
O: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKE2 Represents whether revoking the third Secure Boot key is enabled.

1: Enabled
O: Disabled
(RO)

EFUSE_KEY_PURPOSE_O Represents the purpose of Key0. (RO)

EFUSE_KEY_PURPOSE_1 Represents the purpose of Key1. (RO)
```