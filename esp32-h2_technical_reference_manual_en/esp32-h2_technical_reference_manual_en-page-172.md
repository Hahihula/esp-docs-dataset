

```markdown
Register 5.13. EFUSE_RD_REPEAT_DATA0_REG (0x0030)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | O                                    | Reset                                                                       |
| 30  | EFUSE_RPT4_RESERVED0                | Reserved.                                                                   |
| 29  | EFUSE_RPT4_RESERVED0_1              | Reserved.                                                                   |
| 28  | EFUSE_RPT4_RESERVED0_2              | Reserved.                                                                   |
| 27  | EFUSE_VDD_SPI_AS_GPG_PINS           | SPI AS GPG Pins                                                             |
| 26  | EFUSE_USB_EXCLUDED                   | USB Excluded                                                                |
| 25  | EFUSE_DIS_JTAG_SEL_ENABLE           | JTAG Selection Enable                                                      |
| 24  | EFUSE_SOFT_DIS_JTAG                 | Soft Disable JTAG                                                          |
| 23  | EFUSE_DIS_PAD_JTAG                  | Disable Pad JTAG                                                            |
| 22  | EFUSE_DIS_DIS_MANUAL_ENCRYPT        | Manual Encrypt Disable                                                     |
| 21  | EFUSE_DIS_JTAG_SEL_ENABLE           | JTAG Selection Enable                                                      |
| 20  | EFUSE_SOFT_DIS_JTAG                 | Soft Disable JTAG                                                          |
| 19  | EFUSE_DIS_PAD_JTAG                  | Disable Pad JTAG                                                            |
| 18  | EFUSE_DIS_MANUAL_ENCRYPT            | Manual Encrypt Disable                                                     |
| 17  | EFUSE_DIS_JTAG_SEL_ENABLE           | JTAG Selection Enable                                                      |
| 16  | EFUSE_SOFT_DIS_JTAG                 | Soft Disable JTAG                                                          |
| 15  | EFUSE_DIS_PAD_JTAG                  | Disable Pad JTAG                                                            |
| 14  | EFUSE_DIS_MANUAL_ENCRYPT            | Manual Encrypt Disable                                                     |
| 13  | EFUSE_DIS_JTAG_SEL_ENABLE           | JTAG Selection Enable                                                      |
| 12  | EFUSE_SOFT_DIS_JTAG                 | Soft Disable JTAG                                                          |
| 11  | EFUSE_DIS_PAD_JTAG                  | Disable Pad JTAG                                                            |
| 10  | EFUSE_DIS_MANUAL_ENCRYPT            | Manual Encrypt Disable                                                     |
| 9   | EFUSE_DIS_JTAG_SEL_ENABLE           | JTAG Selection Enable                                                      |
| 8   | EFUSE_SOFT_DIS_JTAG                 | Soft Disable JTAG                                                          |
| 7   | EFUSE_DIS_PAD_JTAG                  | Disable Pad JTAG                                                            |
| 6   | EFUSE_DIS_MANUAL_ENCRYPT            | Manual Encrypt Disable                                                     |
| 5   | EFUSE_DIS_JTAG_SEL_ENABLE           | JTAG Selection Enable                                                      |
| 4   | EFUSE_SOFT_DIS_JTAG                 | Soft Disable JTAG                                                          |
| 3   | EFUSE_DIS_PAD_JTAG                  | Disable Pad JTAG                                                            |
| 2   | EFUSE_DIS_MANUAL_ENCRYPT            | Manual Encrypt Disable                                                     |
| 1   | EFUSE_DIS_JTAG_SEL_ENABLE           | JTAG Selection Enable                                                      |
| 0   | EFUSE_SOFT_DIS_JTAG                 | Soft Disable JTAG                                                          |

EFUSE_RD_DIS Represents whether reading of individual eFuse block (BLOCK4 ~ BLOCK10) is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_RPT4_RESERVED0_4 Reserved. (RO)

EFUSE_DIS_ICACHE Represents whether instruction cache is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_USB_JTAG Represents whether the USB-to-JTAG function is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_POWERGLITCH_EN Represents whether to enable the power glitch detection.
1: Enabled
0: Disabled
(RO)

EFUSE_DIS_FORCE_DOWNLOAD Represents whether the function that forces chip into download mode is disabled.
1: Disabled
0: Enabled
(RO)
```
Continued on the next page...
```