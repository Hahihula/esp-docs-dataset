

```markdown
| Parameters | Bit Width | Hardware Use | Write Protection by EFUSE_WR_DIS Bit Number | Description |
|------------|-----------|--------------|---------------------------------------------|-------------|
| EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE | 1 | N | 16 | Represents whether aggressive revocation of Secure Boot is enabled. |
| EFUSE_FLASH_TPUW | 4 | N | 18 | Represents the flash waiting time after power-up. |
| EFUSE_DIS_DOWNLOAD_MODE | 1 | N | 18 | Represents whether all download modes are disabled. |
| EFUSE_DIS_DIRECT_BOOT | 1 | N | 18 | Represents whether direct boot mode is disabled. |
| EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT | 1 | N | 18 | Represents whether print from USB-Serial-JTAG during ROM boot is disabled. |
| EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE | 1 | N | 18 | Represents whether the USB-Serial-JTAG download function is disabled. |
| EFUSE_ENABLE_SECURITY_DOWNLOAD | 1 | N | 18 | Represents whether security download is enabled. |
| EFUSE_UART_PRINT_CONTROL | 2 | N | 18 | Represents the type of UART printing. |
| EFUSE_FORCE_SEND_RESUME | 1 | N | 18 | Represents whether ROM code is forced to send a resume command during SPI boot. |
| EFUSE_SECURE_VERSION | 16 | N | 18 | Represents the version used by ESP-IDF anti-rollback feature. |
| EFUSE_SECURE_BOOT_DISABLE_FAST_WAKE | 1 | N | 18 | Represents whether FAST VERIFY ON WAKE is disabled or enabled when Secure Boot is enabled. |
| EFUSE_HYS_EN_PAD0 | 6 | Y | 19 | Represents whether to enable the hysteresis function of pad 0-5 |
| EFUSE_HYS_EN_PAD1 | 22 | Y | 19 | Represents whether to enable the hysteresis function of pad 6-27 |
```