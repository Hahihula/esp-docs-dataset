**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Link:**
GoBack

**Subtitle:**
Register 9.13. RTC_CNTL_WAKEUP_STATE_REG (0x0038)

**Diagram/Table Description:**

- **Field Labels and Values in the Diagram:**
  - RTC_CNTL_GPIO_WAKEUP_FILTER
    - (reserved)
    - 0 to 25 bits with values ranging from '0' to '1'
  - RTC_CNTL_WAKEUP_ENA
    - 31, 24, etc.
  - RTC_CNTL_WAKEUP_CAUSE

- **Field Descriptions:**
  - RTC_CNTL_GPIO_WAKEUP_FILTER: Enable filter for GPIO wake-up event. (R/W)
  - RTC_CNTL_WAKEUP_ENA: Wake-up enable bitmap. (R/W)
  - RTC_CNTL_WAKEUP_CAUSE: Wake-up cause. (RO)

**Footer Information:**
Espressif Systems
202 ESP32 TRM (Version 5.6) 
Submit Documentation Feedback