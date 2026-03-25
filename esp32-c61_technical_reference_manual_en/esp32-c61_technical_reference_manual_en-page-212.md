

```markdown
| Parameters                                       | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Description                                                                 |
|--------------------------------------------------|-----------|-------------------------|-----------------------------------------------|-----------------------------------------------------------------------------|
| EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE          | 1         | N                       | 18                                             | Represents whether the USB-Serial-JTAG download function is disabled.       |
| EFUSE_ENABLE_SECURITY_DOWNLOAD                   | 1         | N                       | 18                                             | Represents whether security download is enabled.                            |
| EFUSE_UART_PRINT_CONTROL                         | 2         | N                       | 18                                             | Represents the types of UART printing.                                     |
| EFUSE_FORCE_SEND_RESUME                          | 1         | N                       | 18                                             | Represents whether ROM code is forced to send a resume command during SPI boot.|
| EFUSE_SECURE_VERSION                             | 16        | N                       | 18                                             | Represents the security version used by ESP-IDF anti-rollback feature.      |
| EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE              | 1         | N                       | 19                                             | Represents whether FAST_VERIFY_ON_WAKE is disabled when Secure Boot is enabled.|
```