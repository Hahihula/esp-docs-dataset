

```markdown
Chapter 7 eFuse Controller (EFUSE) GoBack

Register 7.4. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

Continued from the previous page...

EFUSE_SPI_DOWNLOAD_MSPI_DIS Represents whether SPI0 controller during boot_mode_download is disabled.
O: Enabled
1: Disabled
(RO)

EFUSE_DIS_TWAI Represents whether TWAI® function is disabled.
1: Disabled
O: Enabled
(RO)

EFUSE_JTAG_SEL_ENABLE Represents whether the selection of a JTAG signal source through the strapping pin value is enabled when EFUSE_DIS_PAD_JTAG and EFUSE_DIS_USB_JTAG are configured to 0. For more information, please refer to Chapter 10 Chip Boot Control.
1: Enabled
O: Disabled
(RO)

EFUSE_SOFT_DIS_JTAG Represents whether PAD JTAG is disabled in the soft way. It can be restarted via HMAC.
Odd count of bits with a value of 1: Disabled
Even count of bits with a value of 1: Enabled
(RO)

EFUSE_DIS_PAD_JTAG Represents whether PAD JTAG is disabled in the hard way (permanently).
1: Disabled
O: Enabled
(RO)

EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT Represents whether flash encryption is disabled (except in SPI boot mode).
1: Disabled
O: Enabled
(RO)

EFUSE_USB_EXCHG_PINS Represents whether the USB D+ and D- pins is exchanged.
1: Exchanged
O: Not exchanged
(RO)

EFUSE_VDD_SPI_AS_GPIO Represents whether VDD SPI pin is functioned as GPIO.
1: Functioned
O: Not functioned
(RO)

Continued on the next page...
```