

```markdown
| Parameters                  | Bit Width | Hardware Use | Write Protection by EFUSE_WR_DIS Bit Number | Description                                                                                     |
|-----------------------------|---------:|:------------|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| EFUSE_WR_DIS                |    32    | Y           | N/A                                         | Represents whether writing of eFuse bits by eFuse controller is disabled.                      |
| EFUSE_RD_DIS                |     7    | Y           | 0                                           | Represents whether reading data from BLOCK4 ~ 10 in eFuse memory by users is disabled.          |
| EFUSE_DIS_ICACHE            |     1     | Y           | 2                                           | Represents whether instruction cache is disabled.                                               |
| EFUSE_DIS_USB_JTAG          |     1     | Y           | 2                                           | Represents whether the USB-to-JTAG function in the USB module is disabled.                     |
| EFUSE_POWERGLITCH_EN        |     1     | Y           | 2                                           | Represents whether to enable the power glitch detection function.                             |
| EFUSE_DIS_FORCE_DOWNLOAD    |     1     | Y           | 2                                           | Represents whether the function to force the chip into Download mode is disabled.              |
| EFUSE_SPI_DOWNLOAD_MSPI_DIS |     1     | Y           | 17                                          | Represents whether the SPI controller is disabled in boot_mode_download.                      |
| EFUSE_DIS_TWAI              |     1     | Y           | 2                                           | Represents whether the TWAI controller is disabled.                                            |
| EFUSE_JTAG_SEL_ENABLE       |     1     | Y           | 2                                           | Represents whether the selection of a JTAG signal source through the strapping value of GPIO15 is enabled when both EFUSE_DIS_PAD_JTAG and EFUSE_DIS_USB_JTAG are configured to 0. |
| EFUSE_SOFT_DIS_DIS_JTAG     |     3     | Y           | 31                                          | Represents whether JTAG is disabled in the soft way.                                           |
| EFUSE_DIS_PAD_JTAG          |     1     | Y           | 2                                           | Represents whether JTAG is disabled in the hard way (permanently).                             |
| EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT |    1    | Y           | 2                                           | Represents whether flash encryption is disabled (except in SPI boot mode).                     |
| EFUSE_USB_EXCHG_PINS        |     1     | Y           | 30                                          | Represents whether the D+ and D- pins are exchanged.                                          |

Cont'd on next page
```