

```markdown
Register 7.27. EFUSE_RD_REPEAT_DATA_ERR3_REG (0x0188)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0                                                                             |
| 30  | 0                                                                             |
| 29  | 0                                                                             |
| 28  | 0                                                                             |
| 27  | 0                                                                             |
| 26  | EFUSE_XTS_DPA_CLK_ENABLE_ERR (reserved)                                    |
| 25  | EFUSE_XTS_DPA_PSEUDO_LEVEL_ERR                                            |
| 24  | EFUSE_HYS_EN_PAD_ERR                                                       |
| 23  | EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE_ERR                                   |
| 22  | EFUSE_FORCE_SEND_RESUME_ERR                                               |
| 21  | EFUSE_UART_PRINT_CONTROL_ERR                                              |
| 20  | EFUSE_ENABLE_SECURITY_DOWNLOAD_ERR                                        |
| 19  | EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT_ERR                                  |
| 18  | EFUSE_LOCK_KM_KEY_ERR                                                     |
| 17  | EFUSE_DIS_DIRECT_BOOT_ERR                                                 |
| 16  | EFUSE_DIS_DOWNLOAD_MODE_ERR                                               |
| 15  | (reserved)                                                                 |
| 14  | EFUSE_ECDSA_P384_ENABLE_ERR                                                |
| 13  | Reset                                                                      |
| 12  | 0x0                                                                        |
| 11  | 0x0                                                                        |
| 10  | 0                                                                          |
| 9   | 0                                                                          |
| 8   | 0                                                                          |
| 7   | 0                                                                          |
| 6   | 0                                                                          |
| 5   | 0                                                                          |
| 4   | 0                                                                          |
| 3   | 0                                                                          |
| 2   | 0                                                                          |
| 1   | 0                                                                          |
| 0   | 0                                                                          |

EFUSE_DIS_DOWNLOAD_MODE_ERR This bit being 1 represents a programming error of EFUSE_DIS_DOWNLOAD_MODE. (RO)

EFUSE_DIS_DIRECT_BOOT_ERR This bit being 1 represents a programming error of EFUSE_DIS_DIRECT_BOOT. (RO)

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT_ERR This bit being 1 represents a programming error of EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT_ERR. (RO)

EFUSE_LOCK_KM_KEY_ERR Represents the programming error of EFUSE_LOCK_KM_KEY (RO)

EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE_ERR This bit being 1 represents a programming error of EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE. (RO)

EFUSE_ENABLE_SECURITY_DOWNLOAD_ERR This bit being 1 represents a programming error of EFUSE_ENABLE_SECURITY_DOWNLOAD. (RO)

EFUSE_UART_PRINT_CONTROL_ERR Any bit of this field being 1 represents a programming error of EFUSE_UART_PRINT_CONTROL. (RO)

EFUSE_FORCE_SEND_RESUME_ERR This bit being 1 represents a programming error of EFUSE_FORCE_SEND_RESUME. (RO)

EFUSE_SECURE_VERSION_ERR Any bit of this field being 1 represents a programming error of EFUSE_SECURE_VERSION. (RO)

EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE_ERR This bit being 1 represents a programming error of EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE. (RO)

EFUSE_HYS_EN_PAD_ERR This bit being 1 represents a programming error of EFUSE_HYS_EN_PAD. (RO)

EFUSE_XTS_DPA_PSEUDO_LEVEL_ERR Represents the programming error of EFUSE_XTS_DPA_PSEUDO_LEVEL (RO)

EFUSE_XTS_DPA_CLK_ENABLE_ERR Represents the programming error of EFUSE_XTS_DPA_CLK_ENABLE (RO)

EFUSE_ECDSA_P384_ENABLE_ERR Represents the programming error of EFUSE_ECDSA_P384_ENABLE (RO)
```