

```markdown
Chapter 8 eFuse Controller (EFUSE)                                                                 GoBack

Register 8.6. EFUSE_RD_REPEAT_DATA2_REG (0x0038)

Continued from the previous page...

EFUSE_FLASH_TYPE Represents the type of the interfaced flash.
    0: Four data lines
    1: eight data lines
        (RO)

EFUSE_FLASH_PAGE_SIZE Represents flash page size.
    0: 256 bytes
    1: 512 bytes
    2: 1024 bytes
    3: 2048 bytes
        (RO)

EFUSE_FLASH_ECC_EN Represents whether ECC is enabled during flash boot.
    0: Disabled
    1: Enabled
        (RO)

EFUSE_DIS_USB_OTG_DOWNLOAD_MODE Represents whether download via USB-OTG is disabled.
    0: Enabled
    1: Disabled
        (RO)

EFUSE_FLASH_TPUW Represents the flash waiting time after power-up. Measurement unit: ms.
When the value is less than 15, the waiting time is the programmed value. Otherwise, the waiting time is a fixed value, i.e., 30 ms. (RO)
```