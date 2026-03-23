

```markdown
Register 4.13. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30  | EFUSE_VDD_SPI_AS_GPO                |                                                                             |
| 29  | EFUSE_USB_EXCPINS                   |                                                                             |
| 28  | (reserved)                         |                                                                             |
| 27  | EFUSE_DIS_PAD_JTAG                 |                                                                             |
| 26  | EFUSE_DIS_MANUAL_ENCRYPT           |                                                                             |
| 25  | EFUSE_SOFT_DIS_JTAG                |                                                                             |
| 24  | EFUSE_TWI                          |                                                                             |
| 23  | EFUSE_DIS_PTT                      |                                                                             |
| 22  | EFUSE_DIS_RTT                      |                                                                             |
| 21  | EFUSE_DIS_RTC                      |                                                                             |
| 20  | EFUSE_DIS_ICACHE                   |                                                                             |
| 19  | EFUSE_DIS_USB_JTAG                 |                                                                             |
| 18  | EFUSE_DIS_DOWNLOAD_ICACHE          |                                                                             |
| 17  | EFUSE_DIS_USB_SERIAL_JTAG          |                                                                             |
| 16  | EFUSE_DIS_FORCE_DOWNLOAD           |                                                                             |
| 15  | EFUSE_RPT4_RESERVED                |                                                                             |
| 14  | EFUSE_DIS_TWAI                     |                                                                             |
| 13  | EFUSE_JTAG_SEL_ENABLE              |                                                                             |
| 12  | EFUSE_SOFT_DIS_JTAG                |                                                                             |
| 11  | EFUSE_DIS_PAD_JTAG                 |                                                                             |
| 10  | EFUSE_DIS_PTT                      |                                                                             |
| 9   | EFUSE_DIS_RTT                      |                                                                             |
| 8   | EFUSE_DIS_RTC                      |                                                                             |
| 7   | EFUSE_DIS_ICACHE                   |                                                                             |
| 6   | EFUSE_DIS_USB_JTAG                 |                                                                             |
| 5   | EFUSE_DIS_DOWNLOAD_ICACHE          |                                                                             |
| 4   | EFUSE_DIS_USB_SERIAL_JTAG          |                                                                             |
| 3   | EFUSE_DIS_FORCE_DOWNLOAD           |                                                                             |
| 2   | EFUSE_RPT4_RESERVED                |                                                                             |
| 1   | EFUSE_DIS_TWAI                     |                                                                             |
| 0   | EFUSE_RD_DIS                       |                                                                             |

EFUSE_RD_DIS Represents whether users' reading from BLOCK4 ~ 10 is disabled or enabled. 1: Disabled. 0: Enabled. (RO)

EFUSE_DIS_RTC_RAM_BOOT Reserved (used for four backups method). (RO)

EFUSE_DIS_ICACHE Represents whether iCache is disabled or enabled. 1: Disabled. 0: Enabled. (RO)

EFUSE_DIS_USB_JTAG Represents whether the USB-to-JTAG function is disabled. 1: Disabled. 0: Enabled. (RO)

EFUSE_DIS_DOWNLOAD_ICACHE Represents whether iCache is disabled in download mode (boot_mode[3:0] is 0, 1, 2, 3, 6, 7). 1: Disabled. 0: Enabled. (RO)

EFUSE_DIS_USB_SERIAL_JTAG Represents whether USB-Serial-JTAG is disabled. 1: Disabled. 0: Enabled. (RO)

EFUSE_DIS_FORCE_DOWNLOAD Represents whether the function that forces chip into download mode is disabled. 1: Disabled. 0: Enabled. (RO)

EFUSE_RPT4_RESERVED Reserved (used for four backups method). (RO)

EFUSE_DIS_TWAI Represents whether TWAI function is disabled. 1: Disabled. 0: Enabled. (RO)

EFUSE_JTAG_SEL_ENABLE Represents whether to use JTAG directly. 1: Use directly. 0: Not use directly. (RO)

EFUSE_SOFT_DIS_JTAG Represents whether JTAG is disabled in the soft way. Odd count of bits with a value of 1: Disabled. It can still be restarted via HMAC. Even count of bits with a value of 1: Enabled. (RO)

EFUSE_DIS_PAD_JTAG Represents whether JTAG is disabled in the hard way (permanently). 1: Disabled. 0: Enabled. (RO)
```
Continued on the next page...
```