**Chapter Title:**
Chapter 5 eFuse Controller

**Section Heading:**
Register 5.15. EFUSE_RD_REPEAT_DATA2_REG (0x0038)

**Table Description with Labels and Values:**
- EFUSE_FLASH_TPUW (reserved)
- EFUSE_USB_PHY
- EFUSE_STRAP_JTAG
- EFUSE_SECURE_BOOT_EN
- EFUSE_RPT4_RESERVED
- EFUSE_KEY PURPOSE 5
- EFUSE_KEY PURPOSE 3
- EFUSE_KEY PURPOSE 2

**Table Values:**
```
EFUSE_KEY PURPOSE_2 - Represents purpose of Key2. (RO)
EFUSE_KEY PURPOSE_3 - Represents purpose of Kev3. (RO)
EFUSE_KEY PURPOSE_4 - Represents purpose of Key4. (RO)
EFUSE_KEY PURPOSE_5 - Represents purpose of Key5. (RO)
```

**Text Descriptions:**
- EFUSE_RPT4_RESERVED is reserved and used for four backups method.
- EFUSE_SECURE_BOOT_EN represents whether secure boot is enabled or disabled, with 0: Disabled; 1: Enabled
- EFUSE_SECURE_BOOT_AGGRESSIVE_REVOKE indicates if aggressive revoke of secure boot keys is on. Values are either 1: Enabled (RO) or 0: Disabled

**Additional Descriptions and Settings for Other Registers:**
- EFUSE_DIS_USB_JTAG - Indicates whether USB OTG function can be switched to JTAG interface, with values as follows:
  - 0: Disabled; 
  - 1: Enabled
- EFUSE_DIS_USB_SERIAL_JTAG represents if usb_serial_jtag function is disabled or enabled.
- EFUSE_STRAP_JTAG_SEL indicates selection between usb_to_jtag and pad_to_jtag through trapping GPIO3 when both reg_dis_usb_jtag and reg_dis_pad_jtag are equal to 0; 
- EFUSE_USB_PHY_SEL describes the connection relationship for internal PHY, external PHY, USB OTG, or USB Serial/JTAG.
- EFUSE_FLASH_TPUW represents flash waiting time after power-up. The measurement unit is ms.

**Footer:**
Espressif Systems
434 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback