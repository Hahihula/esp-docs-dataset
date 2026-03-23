

```markdown
| Parameters | Bit Width | Accessible by Hardware | Programming-Protection by EFUSE_WR_DIS Bit Number | Description |
|:------------------------------------------|:-----------|:------------------------|:--------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EFUSE_SECURE_BOOT_KEY_REVOKEO | 1 | N | 5 | Represents whether revoking the first Secure Boot key is enabled. |
| EFUSE_SECURE_BOOT_KEY_REVOKE1 | 1 | N | 6 | Represents whether revoking the second Secure Boot key is enabled.. |
| EFUSE_SECURE_BOOT_KEY_REVOKE2 | 1 | N | 7 | Represents whether revoking the third Secure Boot key is enabled. |
| EFUSE_KEY_PURPOSE_0 | 4 | Y | 8 | Represents Key0 purpose, see Table 4.3-2. |
| EFUSE_KEY_PURPOSE_1 | 4 | Y | 9 | Represents Key1 purpose, see Table 4.3-2. |
| EFUSE_KEY_PURPOSE_2 | 4 | Y | 10 | Represents Key2 purpose, see Table 4.3-2. |
| EFUSE_KEY_PURPOSE_3 | 4 | Y | 11 | Represents Key3 purpose, see Table 4.3-2. |
| EFUSE_KEY_PURPOSE_4 | 4 | Y | 12 | Represents Key4 purpose, see Table 4.3-2. |
| EFUSE_KEY_PURPOSE_5 | 4 | Y | 13 | Represents Key5 purpose, see Table 4.3-2. |
| EFUSE_SECURE_BOOT_EN | 1 | N | 15 | Represents whether Secure Boot is enabled. |
| EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE | 1 | N | 16 | Represents whether aggressive revocation of Secure Boot is enabled. |
| EFUSE_FLASH_TPUW | 4 | N | 18 | Represents the flash waiting time after power-up. |
| EFUSE_DIS_DOWNLOAD_MODE | 1 | N | 18 | Represents whether all download modes are disabled. |
| EFUSE_USB_PRINT_CHANNEL | 1 | N | 18 | Represents whether USB printing is disabled. |
| EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE | 1 | N | 18 | Represents whether the USB-Serial-JTAG download function is disabled. |
| EFUSE_ENABLE_SECURITY_DOWNLOAD | 1 | N | 18 | Represents whether UART secure download mode is enabled. |
| EFUSE_UART_PRINT_CONTROL | 2 | N | 18 | Represents the UART boot message output mode. |
| EFUSE_FORCE_SEND_RESUME | 1 | N | 18 | Represents whether ROM code is forced to send a resume command during SPI boot. |
```