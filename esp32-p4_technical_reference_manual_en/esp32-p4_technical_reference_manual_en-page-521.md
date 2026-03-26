

```markdown
Chapter 8 eFuse Controller (EFUSE)

Register 8.26. EFUSE_RD_REPEAT_ERR2_REG (0x0184)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | EFUSE_KEY_PURPOSE_5_ERR | EFUSE_KEY_PURPOSE_4_ERR | EFUSE_KEY_PURPOSE_3_ERR | EFUSE_KEY_PURPOSE_2_ERR |
|     | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | Reset |

EFUSE_KEY_PURPOSE_2_ERR Any bit of this field being 1 represents a programming error of KEY_PURPOSE_2. (RO)

EFUSE_KEY_PURPOSE_3_ERR Any bit of this field being 1 represents a programming error of KEY_PURPOSE_3. (RO)

EFUSE_KEY_PURPOSE_4_ERR Any bit of this field being 1 represents a programming error of KEY_PURPOSE_4. (RO)

EFUSE_KEY_PURPOSE_5_ERR Any bit of this field being 1 represents a programming error of KEY_PURPOSE_5. (RO)

EFUSE_SEC_DPA_LEVEL_ERR Any bit of this field being 1 represents a programming error of SEC_DPA_LEVEL. (RO)

EFUSE_CRYPT_DPA_ENABLE_ERR This bit being 1 represents a programming error of CRYPT_DPA_ENABLE. (RO)

EFUSE_SECURE_BOOT_EN_ERR This bit being 1 represents a programming error of SECURE_BOOT_EN. (RO)

EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE_ERR This bit being 1 represents a programming error of SECURE_BOOT_AGGRESSIVE_REVOKE. (RO)

EFUSE_FLASH_TYPE_ERR This bit being 1 represents a programming error of FLASH_TYPE. (RO)

EFUSE_FLASH_PAGE_SIZE_ERR This bit being 1 represents a programming error of FLASH_PAGE_SIZE. (RO)

EFUSE_FLASH_ECC_EN_ERR This bit being 1 represents a programming error of FLASH_ECC_EN. (RO)

EFUSE_DIS_USB_OTG_DOWNLOAD_MODE_ERR This bit being 1 represents a programming error of DIS_USB_OTG_DOWNLOAD_MODE. (RO)

EFUSE_FLASH_TPUW_ERR This bit being 1 represents a programming error of FLASH_TPUW. (RO)
```