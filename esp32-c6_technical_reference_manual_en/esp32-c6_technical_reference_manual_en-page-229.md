

```markdown
Register 6.96. EFUSE_RD_REPEAT_ERR_REG (0x017C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    | EFUSE_RPTA_RESERVED0_ERR | EFUSE_RPTA_RESERVED1_ERR | EFUSE_RPTA_VDD_SPI_GHG_PNS_ERR | EFUSE_USB_EXCLUDED | EFUSE_DIS_SOFT_DIS_JTAG_ERR | EFUSE_JTAG_SEL_ENABLE_ERR | EFUSE_SPI_DOWNLOAD_MSPI_DIS_ERR | EFUSE_FORCE_DOWNLOAD_ERR | EFUSE_DIS_TWI_ERR | EFUSE_DIS_PAD_JTAG_ERR | EFUSE_DIS_ICACHE_ERR | EFUSE_DIS_USB_JTAG_ERR | EFUSE_DIS_DOWNLOAD_ICACHE_ERR | EFUSE_DIS_USB_SERIAL_JTAG_ERR | EFUSE_SPI_DOWNLOAD_MSPI_DIS_ERR | EFUSE_RD_DIS_ERR | Reset |
| Value | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

EFUSE_RD_DIS_ERR Any bit of this field being 1 represents a programming error of RD_DIS. (RO)

EFUSE_SWAP_UART_SDIO_EN_ERR This bit being 1 represents a programming error of SWAP_UART_SDIO_EN. (RO)

EFUSE_DIS_ICACHE_ERR This bit being 1 represents a programming error of DIS_ICACHE. (RO)

EFUSE_DIS_USB_JTAG_ERR This bit being 1 represents a programming error of DIS_USB_JTAG. (RO)

EFUSE_DIS_DOWNLOAD_ICACHE_ERR This bit being 1 represents a programming error of DIS_DOWNLOAD_ICACHE. (RO)

EFUSE_DIS_USB_SERIAL_JTAG_ERR This bit being 1 represents a programming error of DIS_USB_DEVICE. (RO)

EFUSE_DIS_FORCE_DOWNLOAD_ERR This bit being 1 represents a programming error of DIS_FORCE_DOWNLOAD. (RO)

EFUSE_SPI_DOWNLOAD_MSPI_DIS_ERR This bit being 1 represents a programming error of SPI_DOWNLOAD_MSPI_DIS. (RO)

EFUSE_DIS_TWI_ERR This bit being 1 represents a programming error of DIS_TWI. (RO)

EFUSE_JTAG_SEL_ENABLE_ERR This bit being 1 represents a programming error of JTAG_SEL_ENABLE. (RO)

EFUSE_SOFT_DIS_JTAG_ERR Any bit of this field being 1 represents a programming error of SOFT_DIS_JTAG. (RO)

EFUSE_DIS_PAD_JTAG_ERR This bit being 1 represents a programming error of DIS_PAD_JTAG. (RO)

EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT_ERR This bit being 1 represents a programming error of DIS_DOWNLOAD_MANUAL_ENCRYPT. (RO)

Continued on the next page...
```