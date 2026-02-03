**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Header:**
Register 10.15. RTC_CNTL_INT_RAW_RTC_REG (0x0044)

**Body Text with Descriptions of Interrupts and Registers:**

- **Reset**: 
  - Bit positions from 31 to 0 are listed, each bit is labeled as "Reset".

- **Interrupts Description:**
  - `RTC_CNTL_SLP_WAKEUP_INT_RAW`: Stores the raw interrupt triggered when the chip wakes up from sleep. (RO)
  - `RTC_CNTL_SLP_REJECT_INT_RAW`: Stores the raw interrupt triggered when the chip rejects to go to sleep. (RO)
  - `RTC_CNTL_SDIO_IDLE_INT_RAW`: Stores the raw interrupt triggered when the SDIO idles. (RO)
  - `RTC_CNTL_RTC_WDT_INT_RAW`: Stores the raw RTC watchdog interrupt. (RO)
  - `RTC_CNTL_RTC TOUCH_SCAN_DONE_INT_RAW`: Stores the raw interrupt triggered upon the completion of a touch scanning. (RO)
  - `RTC_CNTL_RTC_ULP_CP_INT_RAW`: Stores the raw ULP co-processor interrupt. (RO)
  - `RTC_CNTL_RTC_TOUCH_DONE_INT_RAW`: Stores the raw interrupt triggered upon the completion of a single touch. (RO)
  - `RTC_CNTL_RTC TOUCH_ACTIVE_INT_RAW`: Stores the raw interrupt triggered when a touch is detected. (RO)
  - `RTC_CNTL_RTC TOUCH_INACTIVE_INT_RAW`: Stores the raw interrupt triggered when a touch is released. (RO)
  - `RTC_CNTL_RTC_BROWN_OUT_INT_RAW`: Stores the raw brown out interrupt. (RO)

**Footer:**
Continued on the next page...

**Page Information at Bottom of Page:**
Espressif Systems
597 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback