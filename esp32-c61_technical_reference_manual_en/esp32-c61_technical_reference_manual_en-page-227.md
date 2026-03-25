

```markdown
Chapter 5 eFuse Controller (EFUSE) GoBack

Register 5.4. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

Continued from the previous page...

EFUSE_JTAG_SEL_ENABLE Represents whether the selection between usb_to_jtag and pad_to_jtag through strapping GPIO15 is disabled when both EFUSE_DIS_PAD_JTAG and EFUSE_DIS_USB_JTAG are configured to 0.

1: Enabled
O: Disabled
(RO)

EFUSE_DIS_PAD_JTAG Represents whether JTAG is disabled in the hard way (permanently).

1: Disabled
O: Enabled
(RO)

EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT Represents whether flash encrypt function is disabled or enabled (except in SPI boot mode).

1: Disabled
O: Enabled
(RO)

EFUSE_USB_DREFH Represents the single-end input threshold Vrefh, ranging from 1.76 V to 2 V, with a step size of 80 mV. (RO)

EFUSE_USB_DREFL Represents the single-end input threshold Vrefl, ranging from 1.76 V to 2 V, with a step size of 80 mV. (RO)

EFUSE_USB_EXCHG_PINS Represents whether the D+ and D- pins is exchanged.

1: Exchanged
O: Not exchanged
(RO)

EFUSE_VDD_SPI_AS_GPIO Represents whether VDD_SPI pin is used as a regular GPIO.

1: Used as a regular GPIO
O: Not used as a regular GPIO
(RO)

EFUSE_WDT_DELAY_SEL Represents the threshold level of the RTC watchdog STGO timeout.

0: Original threshold configuration value of STGO *2
1: Original threshold configuration value of STGO *4
2: Original threshold configuration value of STGO *8
3: Original threshold configuration value of STGO *16
(RO)

EFUSE_SPI_BOOT_CRYPT_CNT Represents whether SPI boot encryption/decryption is enabled.

Odd count of bits with a value of 1: Enabled
Even count of bits with a value of 1: Disabled
(RO)

Continued on the next page...
```