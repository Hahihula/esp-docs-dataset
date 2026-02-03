**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.4. RTC_CNTL_RTC_TIME_UPDATE_REG (0x000C)

**Table Description and Values for Register 10.4:**
- RTC_CNTL_TIMER_SYS_RSTL (reserved)
- RTC_CNTL_TIMER_XTL_OFF
- RTC_CNTL_TIMER_XTL_STALL

**Field Descriptions in Table 10.3-2:**  
- **RTC_CNTL_TIMER SYS STALL**: Selects the triggering condition for the RTC timer.
- **RTC_CNTL_TIMER_XTL OFF**: Selects the triggering condition for the RTC timer (see details in Table 10.3-2).
- **RTC_CNTL_TIMER_SYS_RSTL**: Selects the triggering condition for the RTC timer.

**Section Header:**
Register 10.5. RTC_CNTL_RTC_TIME_LOWO_REG (0x0010)

**Field Description:**  
- **RTC_CNTL_RTC_TIMER_VALUEO_LOW**: Stores the lower 32 bits of RTC timer O.
- **RTC_CNTL_RTC_TIMER_VALUEO_LOW**: Stores the upper 32 bits of RTC timer.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
589 ESP32-S3 TRM (Version 1.7)