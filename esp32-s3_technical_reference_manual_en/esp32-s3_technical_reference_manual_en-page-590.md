**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**GoBack Link:** GoBack

**Register Information:**

- **Register Name and Address:**
  - Register 10.6, RTC_CNTL_RTC_TIME_HIGHO_REG (0x0014)
  
- **Bit Description for RTC_CNTL_RTC_TIMER_VALUEO_HIGH:**
  ```
  31       16      15
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0x00 Reset
  ```

- **Description:**
  - RTC_CNTL_RTC_TIMER_VALUEO_HIGH Stores the higher 16 bits of RTC timer O. (RO)

**Register Information for Register 10.7, RTC_CNTL_RTC_STATEO_REG (0x018):**

- **Bit Description and Functionality Table:** 
  ```
  31       29      28     27
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

  RTC_CNTL_RTC_SLEEP_EN   (WO)
  RTC_CNTL_RTC_REJECT_CAUSE_CLR   (WO)

  RTC_CNTL_APB2RTC_BRIDGE_SEL: APB to RTC using bridge, O: APB to RTC using sync (R/W)
  RTC_CNTL_SDIO_ACTIVE_IND   Indicates the SDIO is active. (RO)
  RTC_CNTL_SLP_WAKEUP   Indicates wakeup events. (R/W)
  RTC_CNTL_SLP_REJECT   Indicates reject-to-sleep event. (R/W)
  RTC_CNTL_SLEEP_EN   Sends the chip to sleep. (R/W)

  RTC_CNTL_RTC_SW_CPU_INT   Sends a SW RTC interrupt to CPU. (WO)
  RTC_CNTL_RTC_SLSP_REJECT_CAUSE_CLR   Clears the RTC reject-to-sleep cause. (WO)
  ```

**Footer:**
- Espressif Systems
- Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)