**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Section Header:**
Register 12.18. TIMG_RTCCALICFG_REG (0x0068)

**Table Description with Labels and Values:**
- TIMG_RTC_CALI_START_CYCLING: Enables periodic frequency calculation.
- TIMG_RTC_CALI_CLK_SEL: Used to select the clock to be calibrated, options include RC_SLOW_CLK or XTAL32K_CLK. (R/W)
- TIMG_RTC_CALI_RDY: Marks the completion of one-shot frequency calculation.
- TIMG_RTC_CALI_MAX: Configures the time to calculate the frequency of RTC slow clock.
- TIMG_RTC_CALI_START: Enables one-shot frequency calculation.

**Register Description and Values for Register 12.19 (TIMG_RTCCALICFG1_REG):**
- TIMG_RTC_CALI_VALUE: When a periodic or oneshot frequency calculation completes, read this value to calculate the frequency of RTC slow clock.
- TIMG_RTC_CALI_CYCLING_DATA_VLD: Marks the completion of periodic frequency calculation.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Reference Number:** 
ESP32-S3 TRM (Version 1.7)