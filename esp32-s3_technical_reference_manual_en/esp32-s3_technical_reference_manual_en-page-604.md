**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Header:**
Register 10.22. RTC_CNTL_RTC_EXT_XTL_CONF_REG (0x0060)

**Table Description:**
- The table lists various register names and their bit positions in the specified register.
- Columns include "Name", "Bits", with values ranging from 'reserved' to specific numbers like 31, 30 through down.

**Body Text:**

- **RTC_CNTL_XTAL32K_WDT_EN**: Set this bit to enable the 32 kHz crystal watchdog. (R/W)
  
- **RTC_CNTL_XTAL32K_WDT_CLK FO**: Set this bit to FPU the 32 kHz crystal watchdog clock. (R/W)

- **RTC_CNTL_XTAL32K_WDT_RESET**: Set this bit to reset the 32 kHz crystal watchdog by SW. (R/W)

- **RTC_CNTL_XTAL32K_EXT_CLK FO**: Set this bit to FPU the external clock of 32 kHz crystal. (R/W)

- **RTC_CNTL_XTAL32K_AUTO_BACKUP**: Set this bit to switch to the backup clock when the 32 kHz crystal is dead. (R/W)

- **RTC_CNTL_XTAL32K_AUTO_RESTART**: Set this bit to restart the 32 kHz crystal automatically when the 32 kHz crystal is dead. (R/W)

- **RTC_CNTL_XTAL32K_AUTO_RETURN**: Set this bit to switch back to 32 kHz crystal when the 32 kHz crystal is restarted. (R/W)

- **RTC_CNTL_XTAL32K_XPDB FORCE**: Set 1 to allow the software to FPD the 32 kHz crystal. Set 0 to allow the FSM to FPD the 32 kHz crystal. (R/W) (R/W)

- **RTC_CNTL_ENCKINIT_XTL_32K**: Applies an internal clock to help the 32 kHz crystal to start. (R/W)

- **RTC_CNTL_DBUF_XTAL_32K O**: single-end buffer: 1 differential buffer (R/W)

- **RTC_CNTL_DGM_XTAL_32K**: xtal_32k gm control (R/W)

**Footer Note:**
Continued on the next page...

**Company Information and Document Version:**
Espressif Systems
604 ESP32-S3 TRM (Version 1.7)