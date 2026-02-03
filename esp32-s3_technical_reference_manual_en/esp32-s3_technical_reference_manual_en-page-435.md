**Title: Chapter 5 eFuse Controller**

**Register Reference:**  
- **Name:** EFUSE_RD_REPEAT_DATA3_REG (0x003C)

**Table Description and Values for Register:**
| Bit | Name                          |
|-----|-------------------------------|
| 31  | EFUSE_DIS_USB_OTG_DOWNLOAD_MODE (reserved) |
| 30  | -                             |
| 29  | -                             |
| ... | ...                           |
| 7   | EFUSE_FOOE_PAGE_SIZE          |
| 6   | EFUSE_FOOE_PIN_POWER_SELECTION |
| 5   | EFUSE_FOOE_PIN_PIN            |
| 4   | EFUSE_FOOE_FLASH_TYPE         |
| 3   | EFUSE_FOOE_FLASH_ECC          |
| 2   | EFUSE_FOOE_FLASH_SIZE         |
| 1   | EFUSE_FOOE.force SEND_RESUME |
| 0   | Reset                         |

**Descriptions of Register Bits:**
- **EFUSE_DIS_USB_OTG_DOWNLOAD_MODE:** Represents whether download mode (boot_mode[3:0]) = {0, 1, 2, 3, 6, 7} is disabled or enabled. {0: Enabled. (RO)}
- **EFUSE_DIS_LEGACY_SPI_BOOT:** Represents whether Legacy SPI boot mode (boot_mode[3:0] = 4) is disabled or enabled. {1: Disabled. 0: Enabled. (RO)}
- **EFUSE_DIS_USB_PRINT:** Represents whether USB printing is disabled or enabled. {1: Disabled. 0: Enabled. (RO)}
- **EFUSE_FLASH_ECC_MODE:** Represents the flash ECC mode in ROM. {0: 16-to-18 byte mode. 1: 16-to-17 byte mode. (RO)}
- **EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE:** Represents whether download through USB-Serial-JTAG is disabled or enabled. {0: Disabled. 1: Enabled. (RO)}
- **EFUSE_ENABLE_SECURITY_DOWNLOAD:** Represents whether secure UART download mode is enabled or disabled (read/write flash only). {1: Enabled. 0: Disabled. (RO)}
- **EFUSE_UART_PRINT_CONTROL:** Represents the default UART boot message output mode. {00: Enabled when GPIO46 is low at reset. 10: Enabled when GPIO46 is high at reset. 11: Disabled. (RO)}
- **EFUSE_PIN_POWER_SELECTION:** Represents the power supply for GPIO33 ~ GPIO37, GPIO47, and GPIO48 while ROM code is executed. {VDD3P3_CPU: VDD_SPI. (RO)}
- **EFUSE_FLASH_TYPE:** Represents the maximum data lines of SPI flash. {0: four lines. 1: eight lines. (RO)}
- **EFUSE_FLASH_PAGE_SIZE:** Represents flash page size. {0: 256 Byte. 1: 512 Byte. 2: 1 KB. 3: 2 KB. (RO)}
- **EFUSE_FLASH_ECC_EN:** Represents whether ECC for flash boot is enabled or disabled. {Enabled. 0: Disabled. (RO)}
- **EFUSE FORCE SEND_RESUME:** Represents whether or not to force ROM code to send a resume command during SPI boot. {1: Send. 0: Not send. (RO)}

**Footer Information:**
- Page number and document version information:
  - "Continued on the next page..."
  - "Espressif Systems"
  - "435 ESP32-S3 TRM (Version 1.7)"
  - Link to submit documentation feedback

(Note: The text above is a summary of what can be extracted from this image, and it does not include any diagrams or flowcharts that may exist in the original document.)