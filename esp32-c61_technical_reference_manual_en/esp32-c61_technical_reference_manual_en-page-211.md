

```markdown
| Parameters                                 | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Description                                                                 |
|--------------------------------------------|-----------|------------------------|----------------------------------------------|-----------------------------------------------------------------------------|
| EFUSE_SPI_BOOT_CRYPT_CNT                  | 3         | Y                      | 4                                            | Represents whether SPI boot encryption/decryption is enabled.               |
| EFUSE_SECURE_BOOT_KEY_REVOKE0             | 1         | N                      | 5                                            | Represents whether revoking first secure boot key is enabled.               |
| EFUSE_SECURE_BOOT_KEY_REVOKE1             | 1         | N                      | 6                                            | Represents whether revoking second secure boot key is enabled.              |
| EFUSE_SECURE_BOOT_KEY_REVOKE2             | 1         | N                      | 7                                            | Represents whether revoking third secure boot key is enabled.               |
| EFUSE_KEY_PURPOSE_0                       | 4         | Y                      | 8                                            | Represents the purpose of Key0.                                             |
| EFUSE_KEY_PURPOSE_1                       | 4         | Y                      | 9                                            | Represents the purpose of Key1.                                             |
| EFUSE_KEY_PURPOSE_2                       | 4         | Y                      | 10                                           | Represents the purpose of Key2.                                             |
| EFUSE_KEY_PURPOSE_3                       | 4         | Y                      | 11                                           | Represents the purpose of Key3.                                             |
| EFUSE_KEY_PURPOSE_4                       | 4         | Y                      | 12                                           | Represents the purpose of Key4.                                             |
| EFUSE_KEY_PURPOSE_5                       | 4         | Y                      | 13                                           | Represents the purpose of Key5.                                             |
| EFUSE_SEC_DPA_LEVEL                       | 2         | Y                      | 14                                           | Represents whether to determine DPA secure level by configuring the clock random frequency dividing mode. |
| EFUSE_SECURE_BOOT_EN                      | 1         | N                      | 16                                           | Represents whether Secure Boot is enabled.                                  |
| EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE       | 1         | N                      | 16                                           | Represents whether aggressive revocation of Secure Boot is enabled.          |
| EFUSE_FLASH_WAITING                       | 4         | N                      | 18                                           | Represents the flash waiting time after power-up, in unit of ms. When the value less than 15, the waiting time is the programmed value. Otherwise, the waiting time is 2 times the programmed value. |
| EFUSE_DIS_DOWNLOAD_MODE                   | 1         | N                      | 18                                           | Represents whether download mode is disabled.                               |
| EFUSE_DIS_DIRECT_BOOT                     | 1         | N                      | 18                                           | Represents whether direct boot mode is disabled.                            |
| EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT       | 1         | N                      | 18                                           | Represents whether print from USB-Serial-JTAG is disabled.                  |
```