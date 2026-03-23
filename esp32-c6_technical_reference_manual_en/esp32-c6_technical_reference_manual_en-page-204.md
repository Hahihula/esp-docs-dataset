

```markdown
Register 6.15. EFUSE_RD_REPEAT_DATA2_REG (0x0038)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | O                                    | OxO                                                                          |
| 28  | O                                    | OxO                                                                          |
| 27  | O                                    | OxO                                                                          |
| 26  | EFUSE_RPT4_RESERVED2_0               | Reserved. (RO)                                                               |
| 25  | EFUSE_FLASH_TPUW                     | Represents the flash waiting time after power-up. Measurement unit: ms. When the value is less than 15, the waiting time is the programmed value. Otherwise, the waiting time is a fixed value, i.e. 30 ms. (RO) |
| 24  | EFUSE_SEC_DPA_LEVEL                  | Represents the security level of anti-DPA attack.<br>0: Security level is SEC_DPA_OFF<br>1: Security level is SEC_DPA_LOW<br>2: Security level is SEC_DPA_MIDDLE<br>3: Security level is SEC_DPA_HIGH<br>For more information, please refer to Chapter 17 System Registers > Section 17.3.2. (RO) |
| 23  | EFUSE_CRYPT_DPA_ENABLE               | Represents whether defense against DPA attack is enabled.<br>1: Enabled<br>0: Disabled (RO) |
| 22  | EFUSE_RPT4_RESERVED2_1               | Reserved. (RO)                                                               |
| 21  | EFUSE_SECURE_BOOT_EN                 | Represents whether Secure Boot is enabled.<br>1: Enabled<br>0: Disabled (RO)     |
| 20  | EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE  | Represents whether aggressive revocation of Secure Boot is enabled.<br>1: Enabled<br>0: Disabled (RO) |
| 19  | O                                    | OxO                                                                          |
| 18  | O                                    | OxO                                                                          |
| 17  | EFUSE_KEY_PURPOSE_5                  | Represents the purpose of Key5. (RO)                                       |
| 16  | EFUSE_KEY_PURPOSE_4                  | Represents the purpose of Key4. (RO)                                       |
| 15  | EFUSE_KEY_PURPOSE_3                  | Represents the purpose of Key3. (RO)                                       |
| 14  | EFUSE_KEY_PURPOSE_2                  | Represents the purpose of Key2. (RO)                                       |
| 13  | O                                    | OxO                                                                          |
| 12  | O                                    | OxO                                                                          |
| 11  | O                                    | OxO                                                                          |
| 10  | O                                    | OxO                                                                          |
| 9   | O                                    | OxO                                                                          |
| 8   | O                                    | OxO                                                                          |
| 7   | O                                    | OxO                                                                          |
| 6   | O                                    | OxO                                                                          |
| 5   | O                                    | OxO                                                                          |
| 4   | O                                    | OxO                                                                          |
| 3   | O                                    | OxO                                                                          |
| 2   | O                                    | OxO                                                                          |
| 1   | O                                    | OxO                                                                          |
| 0   | O                                    | OxO                                                                          |

EFUSE_KEY_PURPOSE_2 Represents the purpose of Key2. (RO)

EFUSE_KEY_PURPOSE_3 Represents the purpose of Key3. (RO)

EFUSE_KEY_PURPOSE_4 Represents the purpose of Key4. (RO)

EFUSE_KEY_PURPOSE_5 Represents the purpose of Key5. (RO)

EFUSE_SEC_DPA_LEVEL Represents the security level of anti-DPA attack.
0: Security level is SEC_DPA_OFF
1: Security level is SEC_DPA_LOW
2: Security level is SEC_DPA_MIDDLE
3: Security level is SEC_DPA_HIGH

For more information, please refer to Chapter 17 System Registers > Section 17.3.2. (RO)

EFUSE_CRYPT_DPA_ENABLE Represents whether defense against DPA attack is enabled.
1: Enabled
0: Disabled (RO)

EFUSE_RPT4_RESERVED2_1 Reserved. (RO)

EFUSE_SECURE_BOOT_EN Represents whether Secure Boot is enabled.
1: Enabled
0: Disabled (RO)

EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE Represents whether aggressive revocation of Secure Boot is enabled.
1: Enabled
0: Disabled (RO)

EFUSE_RPT4_RESERVED2_0 Reserved. (RO)

EFUSE_FLASH_TPUW Represents the flash waiting time after power-up. Measurement unit: ms. When the value is less than 15, the waiting time is the programmed value. Otherwise, the waiting time is a fixed value, i.e. 30 ms. (RO)
```