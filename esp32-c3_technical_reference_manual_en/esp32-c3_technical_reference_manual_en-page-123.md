

```markdown
Register 4.15. EFUSE_RD_REPEAT_DATA2_REG (0x0038)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | O                                    | Ox0                                                                         |
| 28  | O                                    | Ox0                                                                         |
| 27  | O                                    | Ox0                                                                         |
| 26  | EFUSE_KEY_PURPOSE_2                 | Represents purpose of Key2. (RO)                                           |
| 25  | EFUSE_KEY_PURPOSE_3                 | Represents purpose of Key3. (RO)                                           |
| 24  | EFUSE_KEY_PURPOSE_4                 | Represents purpose of Key4. (RO)                                           |
| 23  | EFUSE_KEY_PURPOSE_5                 | Represents purpose of Key5. (RO)                                           |
| 22  | EFUSE_RPT4_RESERVED3                | Reserved (used for four backups method). (RO)                               |
| 21  | EFUSE_SECURE_BOOT_EN                | Represents whether secure boot is enabled or disabled. 1: Enabled. 0: Disabled. (RO) |
| 20  | EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE | Represents whether aggressive revoke of secure boot keys is enabled or disabled. 1: Enabled. 0: Disabled. (RO) |
| 19  | EFUSE_RPT4_RESERVED0                | Reserved (used for four backups method). (RO)                               |
| 18  | EFUSE_FLASH_TPUW                    | Represents flash waiting time after power-up. Measurement unit: ms. If the value is less than 15, the waiting time is the configurable value. Otherwise, the waiting time is always 30 ms. (RO) |
```