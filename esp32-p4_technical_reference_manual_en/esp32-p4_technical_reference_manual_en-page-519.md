

```markdown
| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | EFUSE_RD_REPEAT_ERR_REG                                                     |
| 29  | EFUSE_USB_PHY_SEL_ERR                                                       |
| 28  | EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT_ERR                                      |
| 27  | EFUSE_DIS_PAD_JTAG_ERR                                                      |
| 26  | EFUSE_SOFT_DIS_JTAG_ERR                                                     |
| 25  | EFUSE_JTAG_SEL_ENABLE_ERR                                                   |
| 24  | EFUSE_DIS_TWAI_ERR                                                           |
| 23  | EFUSE_DIS_FORCE_DOWNLOAD_ERR                                                |
| 22  | EFUSE_SPI_DOWNLOAD_MSPI_ERR                                                 |
| 21  | EFUSE_DIS_USB_ITAI_ERR                                                       |
| 20  | EFUSE_DIS_POWERGLITCH_EN_ERR                                                |
| 19  | EFUSE_DIS_USB_JTAG_ERR                                                      |
| 18  | EFUSE_DIS_USB_OTG11_EXCHG_PINS_ERR                                         |
| 17  | EFUSE_DIS_USB_DEVICE_EXCHG_PINS_ERR                                        |
| 16  | EFUSE_RD_DIS_ERR                                                             |
| 15  | (reserved)                                                                   |
| 14  | (reserved)                                                                   |
| 13  | (reserved)                                                                   |
| 12  | (reserved)                                                                   |
| 11  | (reserved)                                                                   |
| 10  | (reserved)                                                                   |
| 9   | (reserved)                                                                   |
| 8   | (reserved)                                                                   |
| 7   | EFUSE_DIS_USB_ITAI_ERR                                                       |
| 6   | EFUSE_DIS_USB_JTAG_ERR                                                       |
| 5   | EFUSE_DIS_USB_OTG11_EXCHG_PINS_ERR                                         |
| 4   | EFUSE_DIS_USB_DEVICE_EXCHG_PINS_ERR                                        |
| 3   | EFUSE_RD_DIS_ERR                                                             |
| 2   | (reserved)                                                                   |
| 1   | (reserved)                                                                   |
| 0   | Reset                                                                        |

EFUSE_RD_DIS_ERR Any bit of this field being 1 represents a programming error of RD_DIS. (RO)

EFUSE_DIS_USB_DEVICE_EXCHG_PINS_ERR This bit being 1 represents a programming error of DIS_USB_DEVICE_EXCHG_PINS. (RO)

EFUSE_DIS_USB_OTG11_EXCHG_PINS_ERR This bit being 1 represents a programming error of DIS_USB_OTG11_EXCHG_PINS. (RO)

EFUSE_DIS_USB_JTAG_ERR This bit being 1 represents a programming error of DIS_USB_JTAG. (RO)

EFUSE_POWERGLITCH_EN_ERR This bit being 1 represents a programming error of POWER-GLITCH_EN. (RO)

EFUSE_DIS_FORCE_DOWNLOAD_ERR This bit being 1 represents a programming error of DIS_FORCE_DOWNLOAD. (RO)

EFUSE_SPI_DOWNLOAD_MSPI_DIS_ERR This bit being 1 represents a programming error of SPI_DOWNLOAD_MSPI_DIS. (RO)

EFUSE_DIS_TWAI_ERR This bit being 1 represents a programming error of DIS_TWAI. (RO)

EFUSE_JTAG_SEL_ENABLE_ERR This bit being 1 represents a programming error of JTAG_SEL_ENABLE. (RO)

EFUSE_SOFT_DIS_JTAG_ERR Any bit of this field being 1 represents a programming error of SOFT_DIS_JTAG. (RO)

EFUSE_DIS_PAD_JTAG_ERR This bit being 1 represents a programming error of DIS_PAD_JTAG. (RO)

EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT_ERR This bit being 1 represents a programming error of DIS_DOWNLOAD_MANUAL_ENCRYPT. (RO)

EFUSE_USB_PHY_SEL_ERR This bit being 1 represents a programming error of USB_PHY_SEL. (RO)
```