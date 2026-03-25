

```markdown
Register 7.7. EFUSE_RD_REPEAT_DATA3_REG (0x003C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 18 | 17 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     |    |    |    |    |    |    |    |    |    |    |   |   |   |   |   |   |   |   |   |
| Description                                                                                                                              |
| EFUSE_ECDSA_P384_ENABLE (reserved)                                               | EFUSE_XTS_DPA_CLK_ENABLE | EFUSE_XTS_DPA_PSEUDO_LEVEL | EFUSE_HYS_EN_PAD | EFUSE_SECURE_ | (reserved)      | EFUSE_FORCE_SEND_RESUME | EFUSE_UART_PRINT_CONTROL | EFUSE_ENABLE_SECURITY_DOWNLOAD_MODE | EFUSE_USB_SERIAL_JTAG_DOWNLOAD_MODE | EFUSE_LOCK_KM_KEY | EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT | EFUSE_DIS_DIRECT_BOOT | EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE |
| 0    | 0x0 | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| Reset                                                                                                                                   |

EFUSE_DIS_DOWNLOAD_MODE Represents whether all Download modes are disabled.
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

EFUSE_LOCK_KM_KEY Represents whether the keys in the Key Manager are locked after deployment.
0: Not locked
1: Locked
(RO)

EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE Represents whether the USB-Serial-JTAG download function is disabled.
1: Disabled
0: Enabled
(RO)

Continued on the next page...
```