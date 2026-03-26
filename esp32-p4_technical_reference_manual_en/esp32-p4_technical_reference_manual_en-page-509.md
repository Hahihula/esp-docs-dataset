

```markdown
Register 8.6. EFUSE_RD_REPEAT_DATA2_REG (0x0038)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 12 | 11 | 8 | 7 | 4 | 3 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    | EFUSE_FLASH_TPUW | EFUSE_DIS_USB_OTG_DOWN | EFUSE_FLASH_ECC_EN | EFUSE_FLASH_SIZE (reserved) | EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE (reserved) | EFUSE_SEC_DPA_LEVEL | EFUSE_KEY_PURPOSE_5 | EFUSE_KEY_PURPOSE_4 | EFUSE_KEY_PURPOSE_3 | EFUSE_KEY_PURPOSE_2 | 0x0 | 0x0 | Reset |
|     |    |    |    |    |    |    |    |    |    |    |    |                |                   |                  |               |                                   |                 |                     |                    |                      |          |         |

EFUSE_KEY_PURPOSE_2 Represents the purpose of Key2. See Table 8.3-2. (RO)

EFUSE_KEY_PURPOSE_3 Represents the purpose of Key3, See Table 8.3-2. (RO)

EFUSE_KEY_PURPOSE_4 Represents the purpose of Key4. See Table 8.3-2. (RO)

EFUSE_KEY_PURPOSE_5 Represents the purpose of Key5. See Table 8.3-2. (RO)

EFUSE_SEC_DPA_LEVEL Represents the security level of anti-DPA attack. The level is adjusted by configuring the clock random frequency division mode.
0: Security level is SEC_DPA_OFF
1: Security level is SEC_DPA_LOW
2: Security level is SEC_DPA_MIDDLE
3: Security level is SEC_DPA_HIGH
(RO)

EFUSE_CRYPTO_DPA_ENABLE Represents whether defense against DPA attack is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_SECURE_BOOT_EN Represents whether Secure Boot is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE Represents whether aggressive revocation of Secure Boot is enabled.
1: Enabled
0: Disabled
(RO)

Continued on the next page...
```