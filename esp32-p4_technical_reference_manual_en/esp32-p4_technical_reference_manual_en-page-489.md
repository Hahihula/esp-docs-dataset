

```markdown
| Parameters                                 | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Description                                                                 |
|---------------------------------------------|---------:|------------------------:|----------------------------------------------|-----------------------------------------------------------------------------|
| EFUSE_USB_PHY_SEL                          | 1        | Y                       | 30                                           | Represents the connection between USB Serial/JTAG Controller, OTG_FS and FS_PHY1, FS_PHY2. |
| EFUSE_XTS_KEY_LENGTH_256                    | 1        | N                       | 1                                            | Represents which key is used for flash encryption.                         |
| EFUSE_WDT_DELAY_SEL                        | 2        | Y                       | 2                                            | Represents RTC watchdog timeout threshold.                                 |
| EFUSE_SPI_BOOT_CRYPT_CNT                   | 3        | Y                       | 4                                            | Represents whether SPI boot encryption/decryption is enabled.               |
| EFUSE_SECURE_BOOT_KEY_REVOKEO              | 1        | N                       | 5                                            | Represents whether revoking the first Secure Boot key is enabled.           |
| EFUSE_SECURE_BOOT_KEY_REVOKE1              | 1        | N                       | 6                                            | Represents whether revoking the second Secure Boot key is enabled.          |
| EFUSE_SECURE_BOOT_KEY_REVOKE2              | 1        | N                       | 7                                            | Represents whether revoking the third Secure Boot key is enabled.           |
| EFUSE_KEY_PURPOSE_0                        | 4        | Y                       | 8                                            | Represents Key0 purpose. See Table 8.3-2.                                   |
| EFUSE_KEY_PURPOSE_1                        | 4        | Y                       | 9                                            | Represents Key1 purpose. See Table 8.3-2.                                   |
| EFUSE_KEY_PURPOSE_2                        | 4        | Y                       | 10                                           | Represents Key2 purpose. See Table 8.3-2.                                   |
| EFUSE_KEY_PURPOSE_3                        | 4        | Y                       | 11                                           | Represents Key3 purpose. See Table 8.3-2.                                   |
| EFUSE_KEY_PURPOSE_4                        | 4        | Y                       | 12                                           | Represents Key4 purpose. See Table 8.3-2.                                   |
| EFUSE_KEY_PURPOSE_5                        | 4        | Y                       | 13                                           | Represents Key5 purpose. See Table 8.3-2.                                   |
| EFUSE_SEC_DPA_LEVEL                        | 2        | Y                       | 14                                           | Represents the security level of anti-DPA (differential power analysis) attack. |
| EFUSE_CRYPT_DPA_ENABLE                     | 1        | Y                       | 14                                           | Represents whether defense against DPA attack is enabled.                   |
| EFUSE_SECURE_BOOT_EN                       | 1        | N                       | 15                                           | Represents whether Secure Boot is enabled.                                  |
| EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE        | 1        | N                       | 16                                           | Represents whether aggressive revocation of Secure Boot is enabled.          |
| EFUSE_FLASH_TYPE                           | 1        | N                       | 18                                           | Represents the type of the interfaced flash.                               |

Cont'd on next page
```