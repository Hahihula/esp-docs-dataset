
```markdown
Register 6.13. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    | EFUSE_VDD_SPI_AS_GSPI_PINS (reserved) | EFUSE_DIS_JTAG_SEL_ENABLE | EFUSE_SOFT_DIS_JTAG | EFUSE_DIS_PAD_JTAG | EFUSE_DIS_MANUAL_ENCRYPT | EFUSE_RPT4_RESERVED0 | EFUSE_RPT4_RESERVED1 | EFUSE_RPTA_RESERVED0 | EFUSE_RPTA_RESERVED2 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| Value | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

EFUSE_RD_DIS Represents whether reading of individual eFuse block (BLOCK4 ~ BLOCK10) is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_SWAP_UART_SDIO_EN Represents whether the pads of UART and SDIO are swapped or not.
1: Swapped
0: Not swapped
(RO)

EFUSE_DIS_ICACHE Represents whether icache is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_USB_JTAG Represents whether the USB-to-JTAG function is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_DOWNLOAD_ICACHE Represents whether iCache is disabled in Download mode.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_USB_SERIAL_JTAG Represents whether USB-Serial-JTAG is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_FORCE_DOWNLOAD Represents whether the function that forces chip into download mode is disabled.
1: Disabled
0: Enabled
(RO)
```