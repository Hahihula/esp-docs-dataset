

```markdown
|31|27|26|25|24|(reserved)|EFUSE_VDD_SPI_AS_GPIO_ERR|EFUSE_USB_EXCHG_PINS_ERR|
|---|---|---|---|---|-----------|--------------------------|-------------------------|
|0| | | | |          |                          |                         |
|21|20|19|18|(reserved)|EFUSE_DIS_PAD_JTAG_ERR|EFUSE_SOFT_DIS_JTAG_ERR|EFUSE_JTAG_SEL_ENABLE_ERR|
||   ||  |           |EFUSE_RPT4_RESERVED_ERR|EFUSE_DIS_FORCE_DOWNLOAD_ERR|EFUSE_DIS_USB_SERIAL_JTAG_ERR|
||   ||  |           |EFUSE_DIS_RTC_RAM_BOOT_ERR|EFUSE_DIS_ICACHE_ERR|EFUSE_DIS_JTAG_ERR|
||   ||  |           |EFUSE_DIS_DIS_ERR|EFUSE_RD_DIS_ERR|                |
```

**Register 4.96. EFUSE_RD_REPEAT_ERR0_REG (0x017C)**

- **EFUSE_RD_DIS_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_RD_DIS. (RO)
- **EFUSE_DIS_RTC_RAM_BOOT_ERR**: Reserved. (RO)
- **EFUSE_DIS_ICACHE_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_ICACHE. (RO)
- **EFUSE_DIS_USB_JTAG_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_USB_JTAG. (RO)
- **EFUSE_DIS_DOWNLOAD_ICACHE_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_DOWNLOAD_ICACHE. (RO)
- **EFUSE_DIS_USB_SERIAL_JTAG_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_USB_SERIAL_JTAG. (RO)
- **EFUSE_DIS_FORCE_DOWNLOAD_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_FORCE_DOWNLOAD. (RO)
- **EFUSE_RPT4_RESERVED_ERR**: Reserved. (RO)
- **EFUSE_DIS_TWAI_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_TWAI. (RO)
- **EFUSE_JTAG_SEL_ENABLE_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_JTAG_SEL_ENABLE. (RO)
- **EFUSE_SOFT_DIS_JTAG_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_SOFT_DIS_JTAG. (RO)
- **EFUSE_DIS_PAD_JTAG_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_PAD_JTAG. (RO)
- **EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT. (RO)
- **EFUSE_USB_EXCHG_PINS_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_USB_EXCHG_PINS. (RO)
- **EFUSE_VDD_SPI_AS_GPIO_ERR**: Any bit in this filed set to 1 indicates that an error occurs in programming EFUSE_VDD_SPI_AS_GPIO. (RO) 147
```