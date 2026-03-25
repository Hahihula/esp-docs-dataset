

```markdown
Register 5.16. EFUSE_RD_REPEAT_DATA3_REG (0x003C)

| Bit | 31 | 26 | 25 | 24 | ... | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|-----|---|---|---|---|---|---|---|---|---|---|
|     |    |    |    |    |      |   |   |   |   |   |   |   |   |   | Reset |
| Value | 0x00 | 0 | ... | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

EFUSE_DIS_DOWNLOAD_MODE Represents whether all download modes are disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_DIRECT_BOOT Represents whether direct boot mode is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT Represents whether print from USB-Serial-JTAG during ROM boot is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_RPT4_RESERVED3_5 Reserved. (RO)

EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE Represents whether the USB-Serial-JTAG download function is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_ENABLE_SECURITY_DOWNLOAD Represents whether security download is enabled. Only UART is supported for download. Reading/writing RAM or registers is not supported (i.e., Stub download is not supported).
1: Enabled
0: Disabled
(RO)
```
Continued on the next page...
```