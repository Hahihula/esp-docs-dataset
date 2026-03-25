

```markdown
| Parameters | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Description |
|:---------------------------------------------|:-----------|:------------------------|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EFUSE_SECURE_BOOT_KEY_REVOKEO                | 1          | N                       | 5                                           | Represents whether revoking Secure Boot key digest 0 is enabled. |
| EFUSE_SECURE_BOOT_KEY_REVOKE1                | 1          | N                       | 6                                           | Represents whether revoking Secure Boot key digest 1 is enabled. |
| EFUSE_SECURE_BOOT_KEY_REVOKE2                | 1          | N                       | 7                                           | Represents whether revoking Secure Boot key digest 2 is enabled. |
| EFUSE_KEY_PURPOSE_0                          | 5          | Y                       | 8                                           | Represents the purpose of Key0. See Table 7.3-2. |
| EFUSE_KEY_PURPOSE_1                          | 5          | Y                       | 9                                           | Represents the purpose of Key1. See Table 7.3-2. |
| EFUSE_KEY_PURPOSE_2                          | 5          | Y                       | 10                                          | Represents the purpose of Key2. See Table 7.3-2. |
| EFUSE_KEY_PURPOSE_3                          | 5          | Y                       | 11                                          | Represents the purpose of Key3. See Table 7.3-2. |
| EFUSE_KEY_PURPOSE_4                          | 5          | Y                       | 12                                          | Represents the purpose of Key4. See Table 7.3-2. |
| EFUSE_KEY_PURPOSE_5                          | 5          | Y                       | 13                                          | Represents the purpose of Key5. See Table 7.3-2. |
| EFUSE_SEC_DPA_LEVEL                          | 2          | Y                       | 14                                          | Represents the security level of anti-DPA attack. The level is adjusted by configuring the clock random frequency division mode. |
| EFUSE_RECOVERY_BOOTLOADER_FLASH_SECTOR_HI    | 3          | N                       | N/A                                         | Represents the starting flash sector (flash sector size is 0x1000) of the recovery bootloader used by the ROM bootloader if the primary bootloader fails. 0 and 0xFFFF - this feature is disabled. (The high part of the field). |
| EFUSE_SECURE_BOOT_EN                         | 1          | N                       | 15                                          | Represents whether Secure Boot is enabled. |
| EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKEO         | 1          | N                       | 16                                          | Represents whether aggressive revocation of Secure Boot is enabled. |
| EFUSE_KM_XTS_KEY_LENGTH_256                  | 1          | N                       | 1                                           | Represents which key flash encryption uses. |
```