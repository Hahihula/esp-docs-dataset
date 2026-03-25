

```markdown
Register 7.6. EFUSE_RD_REPEAT_DATA2_REG (0x0038)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | Omit                                     | Reset                                                                       |
| 31  | Omit                                     | Ox0                                                                          |
| 30  | EFUSE_FLASH_TPUW                         | O                                                                             |
| 29  | EFUSE_KM_XTS_KEY_LENGTH_256              | Represents which key flash encryption uses.                                 |
|     |                                        | 0: XTS-AES-256 key                                                           |
|     |                                        | 1: XTS-AES-128 key                                                           |
| (RO)|
| 28  | EFUSE_SECURE_BOOT_AGRESSIVE_REVOKE       | Represents whether aggressive revocation of Secure Boot is enabled.          |
|     |                                        | 1: Enabled                                                                   |
|     |                                        | 0: Disabled                                                                  |
| (RO)|
| 27  | EFUSE_SECURE_BOOT_EN                     | Represents whether Secure Boot is enabled.                                  |
|     |                                        | 1: Enabled                                                                   |
|     |                                        | 0: Disabled                                                                  |
| (RO)|
| 26  | EFUSE_RECOVERY_BOOTLOADER_FLASH_SECTOR_HI| Represents the starting flash sector (flash sector size is 0x1000) of the recovery bootloader used by the ROM bootloader. If the primary bootloader fails, 0 and 0xFFFF - this feature is disabled. (The high part of the field). (RO) |
|     |                                        |                                                                             |
| 25  | EFUSE_SEC_DPA_LEVEL                      | Represents the security level of anti-DPA attack. The level is adjusted by configuring the clock random frequency division mode.             |
|     |                                        | 0: Security level is SEC_DPA_OFF                                             |
|     |                                        | 1: Security level is SEC_DPA_LOW                                              |
|     |                                        | 2: Security level is SEC_DPA_MIDDLE                                          |
|     |                                        | 3: Security level is SEC_DPA_HIGH                                             |
| (RO)|
| For more information, please refer to Chapter 19 System Registers > Section 19.3.2 Anti-DPA Attack Security Control. |
| 24  | EFUSE_KEY_PURPOSE_5                      | Represents the purpose of Key5. See Table 7.3-2. (RO)                        |
| 23  | EFUSE_KEY_PURPOSE_4                      | Represents the purpose of Key4. See Table 7.3-2. (RO)                        |
| 22  | EFUSE_KEY_PURPOSE_3                      | Represents the purpose of Key3. See Table 7.3-2. (RO)                        |
| 21  | EFUSE_KEY_PURPOSE_2                      | Represents the purpose of Key2. See Table 7.3-2. (RO)                        |
```