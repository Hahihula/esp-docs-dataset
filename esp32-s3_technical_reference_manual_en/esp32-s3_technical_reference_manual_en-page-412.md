**Table Title: Table 5.3-1 – cont'd from previous page**

| Parameters | Bit Width | Accessible by Hardware | Programming-Protection by EFUSE_WR_DIS Bit Number | Description |
|------------|-----------|------------------------|-----------------------------------------------------|-------------|
| EFUSE_WDT_DELAY_SEL | - | Y | 3 | Represents RTC watchdog timeout threshold. |
| EFUSE_SPI_BOOT_CRYPT_CNT | - | Y | 4 | Represents whether SPI boot encrypt/decrypt is disabled. |
| EFUSE_SECURE_BOOT_KEY_REVOKE0 | 1 | N | 5 | Represents whether the first secure boot key is revoked. |
| EFUSE_SECURE_BOOT_KEY_REVOKE1 | 1 | N | 6 | Represents whether the second secure boot key is revoked. |
| EFUSE_SECURE_BOOT_KEY_REVOKE2 | - | Y | 7 | Represents whether the third secure boot key is revoked. |
| EFUSE_KEY_PURPOSE_0 | 4 | Y | 8 | Represents Key0 purpose, see Table 5.3-2. |
| EFUSE_KEY PURPOSE_1 | 4 | Y | 9 | Represents Key1 purpose, see Table 5.3-2. |
| EFUSE_KEY PURPOSE_2 | - | N | 10 | Represents Key2 purpose, see Table 5.3-2. |
| EFUSE_KEY PURPOSE_3 | - | N | 11 | Represents Key3 purpose, see Table 5.3-2. |
| EFUSE_KEY PURPOSE_4 | - | Y | 12 | Represents Key4 purpose, see Table 5.3-2. |
| EFUSE_KEY PURPOSE_5 | - | Y | 13 | Represents Key5 purpose, see Table 5.3-2. |
| EFUSE_SECURE_BOOT_EN | - | N | 15 | Represents whether secure boot is enabled. |
| EFUSE_SECURE_BOOT_AGG_RESSIVE_REVOKE | - | N | 16 | Represents whether aggressive revoke of secure boot keys is enabled. |
| EFUSE_DIS_USB_JTAG | - | Y | 2 | Represents whether the function of usb_serial_jtag that switch usb to jtag is disabled. |
| EFUSE_DIS_USB_SERIAL_JTAG | - | Y | 2 | Represents whether usb_serial_jtag function is disabled. |
| EFUSE_STRAP_JTAG_SEL | - | N | 0 | Represents whether to enable selection between usb_to_jtag or pad_to_jtag through GPIO3. O: pad_to_jtag; 1: usb_to_jtag. |
| EFUSE_USB_PHY_SEL | - | Y | 2 | Represents the connection relationship between internal PHY, external PHY, and USB OTG, USB Serial/JTAG. |
| EFUSE_FLASH_TPUW | - | N | 4 | Represents flash waiting time after power-up. |
| EFUSE_DIS_DOWNLOAD_MODE | - | N | 18 | Represents whether all download modes are disabled. |
| EFUSE_DIS_LEGACY_SPI_BOOT | - | Y | 2 | Represents whether Legacy SPI is disabled.

**Note:** "Cont'd on next page" at the bottom of the table indicates that there may be additional information or parameters listed in a subsequent section not shown here due to pagination constraints.