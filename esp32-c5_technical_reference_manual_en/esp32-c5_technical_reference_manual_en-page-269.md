

```markdown
|31|29|28|27|26|25|24|21|20|19|18|16|15|14|13|12|11|10|9|8|7|6|0|
|:--------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-----------------------------|:------------------------------------------|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
|0xO|0xO| | | | | | | | | |0xO| | | | | | | | | | |Reset|

EFUSE_RD_DIS Represents whether reading of individual eFuse block (BLOCK4 ~ BLOCK10) is disabled. For mapping between the bits of this field and the eFuse blocks, please refer to Table 7.3-3.
1: Disabled
0: Enabled
(RO)

EFUSE_BOOTLOADER_ANTI_ROLLBACK_SECURE_VERSION_HI Represents the anti-rollback secure version of the second stage bootloader used by the first stage (ROM) bootloader (the high part of the field).
(RO)

EFUSE_DIS_ICACHE Represents whether cache is disabled.
1: Disabled
0: Enabled
(RO)

EFUSE_DIS_USB_JTAG Represents whether the USB-to-JTAG function in USB Serial/JTAG is disabled. Note that EFUSE_DIS_USB_JTAG is available only when EFUSE_DIS_USB_SERIAL_JTAG is configured to 0. For more information, please refer to Chapter 10 Chip Boot Control.
1: Disabled
0: Enabled
(RO)

EFUSE_BOOTLOADER_ANTI_ROLLBACK_EN Represents whether the anti-rollback check for the 2nd stage bootloader is enabled.
1: Enabled
0: Disabled
(RO)

EFUSE_DIS_FORCE_DOWNLOAD Represents whether the function that forces chip into Download mode is disabled.
1: Disabled
0: Enabled
(RO)
```