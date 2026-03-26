

```markdown
Chapter 8 eFuse Controller (EFUSE) GoBack


Register 8.4. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30  | EFUSE_USB_PHY_SEL                   | (reserved)                                                                  |
| 29  | EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT   |                                                                             |
| 28  | EFUSE_DIS_PAD_JTAG                  |                                                                             |
| 27  | EFUSE_SOFT_DIS_JTAG                 |                                                                             |
| 26  | EFUSE_JTAG_SEL_ENABLE               |                                                                             |
| 25  | EFUSE_SPI_DWNLOAD_MSPI_DIS          |                                                                             |
| 24  | EFUSE_DIS_FORCE_DOWNLOAD            |                                                                             |
| 23  | (reserved)                          |                                                                             |
| 22  | EFUSE_POWERGLITCH_EN                |                                                                             |
| 21  | EFUSE_USB_JTAG                      |                                                                             |
| 20  | EFUSE_USB_OTG11_EXCHG_PINS          |                                                                             |
| 19  | EFUSE_USB_DEVICE_EXCHG_PINS         |                                                                             |
| 18  | EFUSE_DIS_USB_JTAG                  |                                                                             |
| 17  | (reserved)                          |                                                                             |
| 16  | EFUSE_DIS_TWAI                      |                                                                             |
| 15  | EFUSE_SPI_DOWNLOAD_MSPI_DIS         |                                                                             |
| 14  | EFUSE_DIS_FORCE_DOWNLOAD            |                                                                             |
| 13  | EFUSE_DIS_PAD_JTAG                  |                                                                             |
| 12  | EFUSE_SOFT_DIS_JTAG                 |                                                                             |
| 11  | EFUSE_JTAG_SEL_ENABLE               |                                                                             |
| 10  | EFUSE_SPI_DWNLOAD_MSPI_DIS          |                                                                             |
| 9   | EFUSE_DIS_FORCE_DOWNLOAD            |                                                                             |
| 8   | (reserved)                          |                                                                             |
| 7   | EFUSE_POWERGLITCH_EN                |                                                                             |
| 6   | EFUSE_USB_JTAG                      |                                                                             |
| 5   | EFUSE_USB_OTG11_EXCHG_PINS          |                                                                             |
| 4   | EFUSE_USB_DEVICE_EXCHG_PINS         |                                                                             |
| 3   | (reserved)                          |                                                                             |
| 2   | EFUSE_DIS_USB_JTAG                  |                                                                             |
| 1   | (reserved)                          |                                                                             |
| 0   | EFUSE_RD_DIS                        |                                                                             |

Reset: 0x0

EFUSE_RD_DIS Represents whether reading of individual eFuse block (BLOCK4 ~ BLOCK10) is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_USB_DEVICE_EXCHG_PINS Represents whether the USB Serial/JTAG pins D+ and D- are exchanged.
0: Not exchanged
1: Exchanged
(RO)

EFUSE_USB_OTG11_EXCHG_PINS Represents whether the USB FS pins D+ and D- are exchanged.
0: Not exchanged
1: Exchanged
(RO)

EFUSE_DIS_USB_JTAG Represents whether the USB-to-JTAG function in USB Serial/JTAG is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_POWERGLITCH_EN Represents whether power glitch detection is enabled.
0: Disabled
1: Enabled
(RO)

EFUSE_DIS_FORCE_DOWNLOAD Represents whether the function that forces chip into Download mode is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_SPI_DOWNLOAD_MSPI_DIS Represents accessing MSPI flash/MSPI RAM by SYS AXI matrix is disabled during boot_mode_download.
1: Disabled
0: Enabled
(RO)

Espressif Systems 506 Submit Documentation Feedback ESP32-P4 TRM PRELIMINARY

```