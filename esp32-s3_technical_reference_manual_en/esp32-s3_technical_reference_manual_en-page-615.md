**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Menu:**
GoBack

**Section Title and Description:**

- **Register 10.36. RTC_CNTL_RTC_WDTCONFIG4_REG (0x00A8)**
  - **Field:** Reset
    - **Value:** 0x000fff

- **Description of Field:**
  - RTC_CNTL_WDT_STG3_HOLD Configures the hold time of RTC watchdog at level 4. (R/W)

- **Register 10.37. RTC_CNTL_RTC_WDTFEED_REG (0x00AC)**
  - **Field:** Reset
    - **Value:** 0

- **Description:**
  - RTC_CNTL_RTC_WDT_FEED (reserved)
  
- **Field:**
  - RTC_CNTL_RTC_WDT_FEED Set 1 to feed the RTC watchdog. (WO)

- **Register 10.38. RTC_CNTL_RTC_WDTWPROTECT_REG (0x00B0)**
  - **Field:** Reset
    - **Value:** 0x50d83aa1

- **Description:**
  - If the register contains a different value than 0x50d83aa1, write protection for the RTC watchdog (RWDT) is enabled. (R/W)

**Footer Information:**
Espressif Systems
615 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback