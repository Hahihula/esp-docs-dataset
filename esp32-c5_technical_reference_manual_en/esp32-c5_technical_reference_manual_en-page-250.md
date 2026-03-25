

```markdown
| Parameters | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Description |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------|:------------------------|:--------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EFUSE_WR_DIS | 32 | Y | N/A | Represents whether programming of individual eFuse memory bit is disabled. |
| EFUSE_RD_DIS | 7 | Y | 0 | Represents whether reading of individual eFuse block (BLOCK4 ~ BLOCK10) is disabled. |
| EFUSE_BOOTLOADER_ANTI_ROLLBACK_SECURE_VERSION_HI | 1 | N | N/A | Represents the anti-rollback secure version of the 2nd stage bootloader used by the ROM bootloader (the high part of the field). |
| EFUSE_DIS_ICACHE | 1 | Y | 2 | Represents whether cache is disabled. |
| EFUSE_DIS_USB_JTAG | 1 | Y | 2 | Represents whether the USB-to-JTAG function in USB Serial/JTAG is disabled. |
| EFUSE_BOOTLOADER_ANTI_ROLLBACK_EN | 1 | N | N/A | Represents whether the anti-rollback check for the 2nd stage bootloader is enabled. |
| EFUSE_DIS_FORCE_DOWNLOAD | 1 | Y | 2 | Represents whether the function that forces chip into Download mode is disabled. |
| EFUSE_SPI_DOWNLOAD_MSPI_DIS | 1 | Y | 2 | Represents whether SPI controller during boot_mode_download is disabled. |
| EFUSE_DIS_TWAI | 1 | Y | 2 | Represents whether TWAI® function is disabled. Represents whether the selection of a JTAG signal source through the strapping pin value is enabled when all of EFUSE_DIS_PAD_JTAG and EFUSE_DIS_USB_JTAG are configured to 0. For more information, please refer to Chapter 10 Chip Boot Control. |
| EFUSE_JTAG_SEL_ENABLE | 1 | Y | 2 | Represents whether PAD JTAG is disabled in the soft way. It can be restarted via HMAC. |
| EFUSE_SOFT_DIS_JTAG | 3 | Y | 31 | Cont'd on next page |
```