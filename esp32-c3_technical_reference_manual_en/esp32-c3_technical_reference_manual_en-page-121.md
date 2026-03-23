

```markdown
Chapter 4 eFuse Controller (EFUSE)
GoBack

Register 4.13. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

Continued from the previous page...

EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT Represents whether flash encryption is disabled
(except in SPI boot mode). 1: Disabled. 0: Enabled. (RO)

EFUSE_USB_EXCHG_PINS Represents whether or not USB D+ and D- pins are swapped. 1:
Swapped. 0: Not swapped. (RO)

Note: The eFuse has a design flaw and does not move the pullup (needed to detect USB
speed), resulting in the PC thinking the chip is a low-speed device, which stops
communication. For detailed information, please refer to Chapter 30 USB Serial/JTAG
Controller (USB_SERIAL_JTAG).

EFUSE_VDD_SPI_AS_GPIO Represents whether the VDD_SPI pin is used as a regular GPIO.
1: Used as a regular GPIO. 0: Not used as a regular GPIO. (RO)
```