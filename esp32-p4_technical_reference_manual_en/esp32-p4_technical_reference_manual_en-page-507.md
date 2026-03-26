

```markdown
Register 8.5. EFUSE_RD_REPEAT_DATA1_REG (0x0034)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    | O  | O  | O  | O  | O  | O  | O  | O  | O  | O  | x  |
| Value | 0x0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | (reserved) | EFUSE_SPI_BOOT_CRYPT_CNT | EFUSE_WDT_DELAY_SEL | (reserved) | EFUSE_XTS_KEY_LENGTH_256 |
| Reset |    |    |    |    |    |    |    |    |    |    |    |    |            |                  |               |              |                   |

EFUSE_XTS_KEY_LENGTH_256 Represents which key is used for flash encryption.
0: XTS-256 key. Key length: 512 bits.
1: XTS-128 key. Key length: 256 bits.
(RO)

EFUSE_WDT_DELAY_SEL Represents RTC watchdog timeout threshold.
0: The originally configured STGO threshold × 2
1: The originally configured STGO threshold × 4
2: The originally configured STGO threshold × 8
3: The originally configured STGO threshold × 16
(RO)

EFUSE_SPI_BOOT_CRYPT_CNT Represents whether SPI boot encryption/decryption is enabled.
Odd count of bits with a value of 1: Enabled
Even count of bits with a value of 1: Disabled
(RO)

EFUSE_SECURE_BOOT_KEY_REVOKEO Represents whether revoking Secure Boot key O is enabled.
1: Enabled
0: Disabled
(RO)
```