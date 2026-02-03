**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Subtitle:**
Register 10.60. RTC_CNTL_INT_ENA_RTC_W1TS_REG (0x0138)

**Body Text with Descriptions of Register Bits and Their Functions:**

- **RTC_CNTL_SLP_WAKEUP_INT_ENA_W1TS**: Enables interrupt when the chip wakes up from sleep.
  - If value is written to this bit, the RTC_CNTL_SLP_WAKEUP_INT_ENA field will be set to 1.

- **RTC_CNTL_SLP_REJECT_IEN_W1TS**: Enables interrupt when the chip rejects go to sleep.
  - If value is written to this bit, the RTC_CNTL_SLP_REJECT_INT_ENA field will be set to 1.

- **RTC_CNTL_SDIO_IDLE_INT_ENA_W1TS**: Enables interrupt when the SDIO idles.
  - If value is written to this bit, the RTC_CNTL_SDIO_IDLE_INT_ENA field will be set to 1.

- **RTC_CNTL_RTC_WDT_INT_ENA_W1TS**: Enables the RTC watchdog interrupt.
  - If value is written to this bit, the RTC_CNTL_RTC_WDT_INT_ENA field will be set to 1.

- **RTC_CNTL_RTC TOUCH_SCAN_DONE_INT_ENA_W1TS**: Enables interrupt upon completion of a touch scanning.
  - If value is written to this bit, the RTC_CNTL_RTC_TOUCH_SCAN_DONE_INT_ENA field will be set to 1.

- **RTC_CNTL_RTC_ULP_CP_INT_ENA_W1TS**: Enables the ULP co-processor interrupt.
  - If value is written to this bit, the RTC_CNTL_RTC_ULP_CP_INT_ENA field will be set to 1.

- **RTC_CNTL_RTC_TOUCH_DONE_INT_ENA_W1TS**: Enables interrupt upon completion of a single touch.
  - If value is written to this bit, the RTC_CNTL_RTC TOUCH DONE INT ENA field will be set to 1.

- **RTC_CNTL_RTC_TOUCH_ACTIVE_INT_ENA_W1TS**: Enables interrupt when a touch is detected.
  - If value is written to this bit, the RTC_CNTL_RTC_TOUCH ACTIVE INT ENA field will be set to 1.

- **RTC_CNTL_RTC_TOUCH_INACTIVE_INT_ENA_W1TS**: Enables interrupt when a touch is released.
  - If value is written to this bit, the RTC_CNTL_RTC TOUCH INACTIVE INT ENA field will be set to 1.

**Footer:**
Continued on the next page...

**Additional Information at Bottom of Page:**
Espressif Systems
629 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback