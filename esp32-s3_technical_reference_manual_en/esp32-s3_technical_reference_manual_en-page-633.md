**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Register Information for RTC_CNTL RETENTION_CTRL_REG (0x0140):**

- **Field Descriptions and Values in Binary:**
  - RTC_CNTL_RETENTION_WAIT [31, 25]: Reserved.
  - RTC_CNTL_RETENTION_EN [24, 23]: Reserved.
  - RTC_CNTL_RETENTION_CLKOFF_WAIT [20, 19]: Reserved.
  - RTC_CNTL_RETENTION_DONE_WAIT [17, 16]: Reserved.
  - RTC_CNTL_RETENTION_TARGET [15, 14]: Reserved.

- **Field Descriptions:**
  - RTC_CNTL_RETENTION_TARGET: Configures retention target: cpu and/or tag (R/W)
  - RTC_CNTL_RETENTIONDone_WAIT: Configures the waiting cycle before retention done (R/W)
  - RTC_CNTL_RETENTION_CLKOFF_WAIT: Configures the waiting cycle before clk_off. (R/W)
  - RTC_CNTL_RETENTION_EN: Set this bit to enable retention. (R/W)
  - RTC_CNTL_RETENTION_WAIT: Configures the waiting cycles for retention operation. (R/W)

**Register Information for RTC_CNTL_RTC_FIB_SEL_REG (0x0148):**

- **Field Descriptions and Values in Binary:**
  - RTC_CNTL_RTC_FIB_SEL [3, 2]: Reserved.
  - RTC_CNTL_RTC_FIB_SEL [7]: Reserved.

- **Field Description:**
  - RTC_CNTL_RTC_FIB_SEL: Configures the brownout detector. (R/W)

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback