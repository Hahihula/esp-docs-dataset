

```markdown
Chapter 5 eFuse Controller (EFUSE)
GoBack

Register 5.4. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | EFUSE_SECURE_BOOT_KEY_REV0_2         |                                                                             |
| 29  | EFUSE_SECURE_BOOT_KEY_REV0_1         |                                                                             |
| 28  | EFUSE_SECURE_BOOT_KEY_REV0_O         |                                                                             |
| 27  | EFUSE_WDT_DELAY_SEL                  |                                                                             |
| 26  | EFUSE_VDD_USB_SPI_AS_OPO             |                                                                             |
| 25  | EFUSE_USB_EXCHG_PINS                 |                                                                             |
| 24  | EFUSE_USB_DRELF                      |                                                                             |
| 23  | EFUSE_DIS_USB_DREFH                  |                                                                             |
| 22  | EFUSE_SPI_DOWNLOAD_ENABLE            |                                                                             |
| 21  | EFUSE_SPI_DOWNLOAD_MSPI_DIS          |                                                                             |
| 20  | EFUSE_SPI_DOWNLOAD_JTAG_DIS          |                                                                             |
| 19  | EFUSE_SPI_SERIAL_JTAG_DIS            |                                                                             |
| 18  | EFUSE_DIS_ICACHE                     |                                                                             |
| 17  | EFUSE_DIS_USB_JTAG                  |                                                                             |
| 16  | EFUSE_DIS_USB_SERIAL_JTAG           |                                                                             |
| 15  | EFUSE_DIS_FORCE_DOWNLOAD             |                                                                             |
| 14  | EFUSE_SPI_DOWNLOAD_MSPI_DIS          |                                                                             |
| 13  | boot_mode_download                   |                                                                             |
| 12  | 1: Disabled                          |                                                                             |
| 11  | 0: Enabled                           |                                                                             |
| 10  | (RO)                                 |                                                                             |
| 9   | O                                    |                                                                             |
| 8   | O                                    |                                                                             |
| 7   | O                                    |                                                                             |
| 6   | EFUSE_RD_DIS                         |                                                                             |
| 5   | Reset                                |                                                                             |
| 4   | O                                    |                                                                             |
| 3   | O                                    |                                                                             |
| 2   | O                                    |                                                                             |
| 1   | O                                    |                                                                             |
| 0   | O                                    |                                                                             |

EFUSE_RD_DIS Represents whether reading of individual eFuse block (BLOCK4 ~ BLOCK10) is disabled or enabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_ICACHE Represents whether iCache is disabled or enabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_USB_JTAG Represents whether the function of USB-to-JTAG is disabled or enabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_USB_SERIAL_JTAG Represents whether USB-Serial-JTAG is disabled or enabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_FORCE_DOWNLOAD Represents whether the function that forces chip into download mode is disabled or enabled.
1: Disabled
0: Enabled
(RO)

EFUSE_SPI_DOWNLOAD_MSPI_DIS Represents whether SPI controller is disabled during boot_mode_download.
1: Disabled
0: Enabled
(RO)

Continued on the next page...
```