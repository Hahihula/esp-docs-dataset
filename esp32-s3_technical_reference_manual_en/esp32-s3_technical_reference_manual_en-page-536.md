**Chapter Title:**
Chapter 8 Chip Boot Control

**Body Text with List Items and Subsections**

- If this eFuse is **0 (default)**, software can force switch the chip from SPI Boot mode to Joint Download Boot mode by setting register `RTC_CNTL FORCE DOWNLOAD_BOOT` and triggering a CPU reset. In this case, hardware overwrites `GPIO STRAPPING [3:2]` from "1x" to "00".
- If this eFuse is **1**, `RTC_CNTL FORCE DOWNLOAD_BOOT` is disabled. `GPIO STRAPPING` can not be overwritten.

**Subsection Title:** EFUSE_DIS_DOWNLOAD_MODE

- If this eFuse is 1, Joint Download Boot mode is disabled.
  - `GPIO STRAPPING` will not be overwritten by `RTC_CNTL FORCE DOWNLOAD_BOOT`

**Subsection Title:** EFUSE_ENABLE_SECURITY_DOWNLOAD

- If this eFuse is set to **1**, the secure download mode is enabled, allowing reading, writing, and erasing plaintext flash. However, it does not permit downloading code to flash for direct execution via UART, USB, or SPI interfaces; register operations are supported.
  - Note that in this mode, the supported `esptool` commands are limited: For example, writing to flash is allowed but reading is not.

**Note:** To read flash, please switch to SPI Boot mode and enable the bootloader. Ignore eFuse if Joint Download Boot mode is disabled.

- If this eFuse is **1**, Direct Boot mode is disabled.
  - USB Serial/JTAG Controller can also force the chip into Joint Download Boot mode from SPI Boot mode as well as force the chip into SPI Boot mode from Joint Download Boot mode for detailed information, please refer to Chapter [33](#) `USB Serial/JTAG Controller (USB_SERIAL_JTAG)`.

**Subsection Title:** 8.3 ROM Messages Printing Control

- During the boot process, ROM messages are printed to both UARTO and USB Serial/JTAG controller by default.
- The printing to UARTO or USB Serial/JTAG controller can be disabled in various boot modes or configuration:
  - Printing to UARTO is controlled as described in the table below.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:** 
536