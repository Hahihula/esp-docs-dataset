

```markdown
Chapter 8 eFuse Controller (EFUSE)

Register 8.25. EFUSE_RD_REPEAT_ERR1_REG (0x0180)
```

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | EFUSE_XTS_KEY_LENGTH_256_ERR | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | (reserved) | (reserved) |
|     |    |    |    |                          |    |    |    |    |    |    |    |    | EFUSE_WDT_DELAY_SEL_ERR | EFUSE_SPI_BOOT_CRYPTO_CNT_ERR | EFUSE_SECURE_BOOT_KEY_REVOKEO_ERR | EFUSE_SECURE_BOOT_KEY_REVOKE1_ERR | EFUSE_SECURE_BOOT_KEY_REVOKE2_ERR | EFUSE_KEY_PURPOSE_O_ERR | EFUSE_KEY_PURPOSE_1_ERR |

EFUSE_XTS_KEY_LENGTH_256_ERR This bit being 1 represents a programming error of XTS_KEY_LENGTH_256. (RO)

EFUSE_WDT_DELAY_SEL_ERR Any bit of this field being 1 represents a programming error of WDT_DELAY_SEL. (RO)

EFUSE_SPI_BOOT_CRYPTO_CNT_ERR Any bit of this field being 1 represents a programming error of SPI_BOOT_CRYPTO_CNT. (RO)

EFUSE_SECURE_BOOT_KEY_REVOKEO_ERR This bit being 1 represents a programming error of SECURE_BOOT_KEY_REVOKEO. (RO)

EFUSE_SECURE_BOOT_KEY_REVOKE1_ERR This bit being 1 represents a programming error of SECURE_BOOT_KEY_REVOKE1. (RO)

EFUSE_SECURE_BOOT_KEY_REVOKE2_ERR This bit being 1 represents a programming error of SECURE_BOOT_KEY_REVOKE2. (RO)

EFUSE_KEY_PURPOSE_O_ERR Any bit of this field being 1 represents a programming error of KEY_PURPOSE_O. (RO)

EFUSE_KEY_PURPOSE_1_ERR Any bit of this field being 1 represents a programming error of KEY_PURPOSE_1. (RO)
```