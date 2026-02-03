**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.39. RTC_CNTL_RTC_SWD_CONF_REG (0x00B4)

**Table Description:**
- The table lists various registers related to the RTC_CNTL_RTC_SWD_CONF_REG register, including their bit positions and descriptions.

**Text Content with Descriptions of Registers:**

- **RTC_CNTL_SWD_RESET_FLAG**: Indicates the super watchdog reset flag. (RO)
  
- **RTC_CNTL_SWD_FEED_IN**: Receiving this interrupt leads to feeding the super watchdog via SW. (RO)

- **RTC_CNTL_SWD_BYPASS_RST**: Set this bit to enable super watchdog reset. (R/W)

- **RTC_CNTL_SWD_SIGNAL_WIDTH**: Adjusts the signal width sent to the super watchdog. (R/W)

- **RTC_CNTL_SWD_RST_FLAG_CLR**: Set to reset the super watchdog reset flag. (WO)

- **RTC_CNTL_SWD_FEED**: Set to feed the super watchdog via SW. (WO)

- **RTC_CNTL_SWD_DISABLE**: Set this bit to disable super watchdog. (RW)

- **RTC_CNTL_SWD_AUTO_FEED_EN**: Set this bit to enable automatic watchdog feeding upon interrupts. (R/W)

**Register 10.40: RTC_CNTL_RTC_SWD_WPROTECT_REG (0x00B8)**

- **RTC_CNTL_SWD_WKEY**: Sets the write protection key of the super watchdog. (R/W)

**Footer Information:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)