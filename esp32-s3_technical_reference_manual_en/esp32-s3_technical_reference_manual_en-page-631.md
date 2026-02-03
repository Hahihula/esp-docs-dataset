**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Subtitle:**
Register 10.61. RTC_CNTL_INT_ENA_RTC_W1TC_REG (0x013C)

**Body Text with Descriptions of Register Bits and Their Functions:**

- **Bit 31:** Reset
- **Bit 29 to Bit 8:** Reserved

**Description for Each Bit Field in the Register:**
- **RTC_CNTL_SLP_WAKEUP_INT_ENA_W1TC**: Clears the interrupt triggered when the chip wakes up from sleep. If the value is written to this bit, the RTC_CNTL_SLP_WAKEUP_INT_CLR field will be cleared.
  - (WO)
  
- **RTC_CNTL_SLP_REJECT_INT_ENA_W1TC**: Clears the interrupt triggered when the chip rejects to go sleep. If the value is written to this bit, the RTC_CNTL_SLP_REJECT_INT_CLR field will be cleared.
  - (WO)

- **RTC_CNTL_SDIO_IDLE_INT_ENA_W1TC**: Clears the interrupt triggered when the SDIO idles. If the value 1 is written to this bit, the RTC_CNTL_SDIO_IDLE_INT_CLR field will be cleared.
  - (WO)
  
- **RTC_CNTL_RTC_WDT_INT_ENA_W1TC**: Clears the RTC watchdog interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_WDT_INT_CLR field will be cleared.
  - (WO)

- **RTC_CNTL_RTC TOUCH_SCAN_DONE_INT_ENA_W1TC**: Clears the interrupt triggered upon completion of a touch scanning. If the value 1 is written to this bit, the RTC_CNTL_RTC_TOUCH_SCAN_DONE_INT_CLR field will be cleared.
  - (WO)
  
- **RTC_CNTL_RTC_ULP_CP_INT_ENA_W1TC**: Clears the ULP co-processor interrupt. If the value 1 is written to this bit, the RTC_CNTL_RTC_ULP_CP_INT_CLR field will be cleared
  - (WO)

- **RTC_CNTL_RTC_TOUCH_DONE_INT_ENA_W1TC**: Clears the interrupt triggered upon completion of a single touch. If the value 1 is written to this bit, the RTC_CNTL_RTC TOUCH DONE INT_CLR field will be cleared.
  - (WO)
  
- **RTC_CNTL_RTC TOUCH ACTIVE_INT_ENA_W1TC**: Clears the interrupt triggered when a touch is detected. If the value 1 is written to this bit, the RTC_CNTL_RTC TOUCH ACTIVE INT_CLR field will be cleared
  - (WO)

**Footer:**
Continued on the next page...

**Document Information at Bottom of Page:**
Espressif Systems  
631  
Submit Documentation Feedback

**Document Version Note:** ESP32-S3 TRM (Version 1.7)