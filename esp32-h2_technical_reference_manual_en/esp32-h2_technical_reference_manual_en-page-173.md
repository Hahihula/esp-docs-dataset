

```markdown
Chapter 5 eFuse Controller (EFUSE) GoBack

Register 5.13. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

Continued from the previous page...

EFUSE_SPI_DOWNLOAD_MSPI_DIS Represents whether SPI controller is disabled during boot_mode_download.
1: Disabled
O: Enabled
(RO)

EFUSE_DIS_TWAI Represents whether TWAI function is disabled.
1: Disabled
O: Enabled
(RO)

EFUSE_ITAG_SEL_ENABLE Represents whether the selection of a JTAG signal source through the strapping value of GPIO25 is enabled when both EFUSE_DIS_PAD_JTAG and EFUSE_DIS_USB_JTAG are configured to O.
1: Enabled
O: Disabled
(RO)

EFUSE_SOFT_DIS_JTAG Represents whether JTAG is disabled in the soft way. It can be restarted via HMAC.
Odd count of bits with a value of 1: Disabled
Even count of bits with a value of 1: Enabled
(RO)

EFUSE_DIS_PAD_JTAG Represents whether JTAG is disabled in the hard way (permanently).
1: Disabled
O: Enabled
(RO)

EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT Represents whether flash encryption is disabled (except in SPI boot mode).
1: Disabled
O: Enabled
(RO)

EFUSE_USB_EXCHG_PINS Represents whether the D+ and D- pins are exchanged.
1: Exchanged
O: Not exchanged
(RO)

EFUSE_VDD_SPI_AS_GPIO Represents whether the VDD_SPI pin is used as a regular GPIO.
1: Used as a regular GPIO
O: Not used as a regular GPIO
(RO)

Continued on the next page...
```