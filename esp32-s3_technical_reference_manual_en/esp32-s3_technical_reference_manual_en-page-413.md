**Title:**
Table 5.3-1 – cont'd from previous page

**Columns:**
- Parameters
- Bit Width
- Accessible by Hardware
- Programming-Protection by EFUSE_WR_DIS Bit Number
- Description

**Rows:**

1. **EFUSE_DIS_USB_PRINT**
   - 1
   - N
   - 18
   - Represents whether USB printing is disabled.

2. **EFUSE_FLASH_ECC_MODE**
   - 1
   - N
   - 18
   - Represents the flash ECC mode in ROM.

3. **EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE**
   - 1
   - N
   - 18
   - Represents whether download through USB-Serial-JTAG is disabled.

4. **EFUSE_ENABLE_SECURITY_DOWNLOAD**
   - 1
   - N
   - 18
   - Represents whether secure UART download mode is enabled.

5. **EFUSE_UART_PRINT_CONTROL**
   - 2
   - N
   - 18
   - Represents the default UART boot message output mode.

6. **EFUSE_PIN_POWER_SELECTION**
   - 1
   - N
   - 18
   - Represents the power supply for GPIO33 ~ GPIO37, GPIO47, and GPIO48.

7. **EFUSE_FLASH_TYPE**
   - 1
   - N
   - 18
   - Represents the maximum data lines of SPI flash.

8. **EFUSE_FLASH_PAGE_SIZE**
   - 2
   - N
   - 18
   - Represents the page size of flash.

9. **EFUSE_FLASH_ECC_EN**
   - 1
   - N
   - 18
   - Represents whether ECC for flash boot is enabled.

10. **EFUSE FORCE SEND_RESUME**
    - 1
    - N
    - 18
    - Represents whether to force ROM code to send a resume command during SPI boot.

11. **EFUSE_SECURE_VERSION**
    - 16
    - N
    - 18
    - Represents IDF secure version.

12. **EFUSE_DIS_USB_OTG_DOWNLOAD_MODE**
    - 1
    - N
    - 19
    - Represents whether download through USB-OTG is disabled.

**Footer:**
ESP32-S3 TRM (Version 1.7)