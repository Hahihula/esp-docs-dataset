

```markdown
Chapter 8 eFuse Controller (EFUSE) GoBack

Register 8.7. EFUSE_RD_REPEAT_DATA3_REG (0x003C)

| Bit | 31 | 27 | 26 | 25 | 24 | ... | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|-----|---|---|---|---|---|---|---|---|---|---|
|     |    |    |    |    |    |      |   |   |   |   |   |   |   |   |   |   |
| Value | 0x0 | 0 | 0 | ... | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

EFUSE_DIS_DOWNLOAD_MODE Represents whether all Download modes are disabled.
1: Disabled
O: Enabled
(RO)

EFUSE_DIS_DIRECT_BOOT Represents whether direct boot mode is disabled.
1: Disabled
O: Enabled
(RO)

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT Represents whether print from USB-Serial-JTAG during ROM boot is disabled.
1: Disabled
O: Enabled
(RO)

EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE Represents whether the USB-Serial-JTAG download function is disabled.
1: Disabled
O: Enabled
(RO)

EFUSE_ENABLE_SECURITY_DOWNLOAD Represents whether security download is enabled. Only UART is supported for download. Reading/writing RAM or registers is not supported (i.e., stub download is not supported).
1: Enabled
O: Disabled
(RO)

Continued on the next page...
```