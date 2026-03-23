

```markdown
Register 4.14. EFUSE_RD_REPEAT_DATA1_REG (0x0034)

| 31 | 28 | 27 | 24 | 23 | 22 | 21 | 20 | 18 | 17 | 16 | 15 |
|-----|----:|:------------------------|:---------------------------------------------|:----------------------------------------------------------|:------------------------------------------------------------------|
| 0xO |    | EFUSE_KEY_PURPOSE_1     | EFUSE_KEY_PURPOSE_O                           | EFUSE_SECURE_BOOT_KEY_REVOKE2                              | EFUSE_SPI_BOOT_CRYPTO_CNT                                     |
|     |    |                        |                                             | EFUSE_SECURE_BOOT_KEY_REVOKE1                             | EFUSE_WDT_DELAY_SEL                                          |
|     |    |                        |                                             | EFUSE_SECURE_BOOT_KEY_REVOKEO                            | EFUSE_RPT4_RESERVED2                                         |

EFUSE_RPT4_RESERVED2 Reserved (used for four backups method). (RO)

EFUSE_WDT_DELAY_SEL Represents RTC watchdog timeout threshold. Measurement unit: slow clock cycle. 00: 400000, 01: 80000, 10: 160000, 11:320000. (RO)

EFUSE_SPI_BOOT_CRYPTO_CNT Represents whether SPI boot encrypt/decrypt is disabled or enabled. Odd count of bits with a value of 1: Enabled. Even count of bits with a value of 1: Disabled. (RO)

EFUSE_SECURE_BOOT_KEY_REVOKEO Represents whether or not the first secure boot key is revoked. 1: Revoked. 0: Not revoked. (RO)

EFUSE_SECURE_BOOT_KEY_REVOKE1 Represents whether or not the second secure boot key is revoked. 1: Revoked. 0: Not revoked. (RO)

EFUSE_SECURE_BOOT_KEY_REVOKE2 Represents whether or not the third secure boot key is revoked. 1: Revoked. 0: Not revoked. (RO)

EFUSE_KEY_PURPOSE_O Represents purpose of KeyO. (RO)

EFUSE_KEY_PURPOSE_1 Represents purpose of Key1. (RO)
```