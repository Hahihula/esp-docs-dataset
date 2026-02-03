**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.8. RTC_CNTL_RTC_TIMER1_REG (0x01C)

**Table Description for Register 10.8:**
- **Columns:** Bits, Values in hexadecimal.
- **Rows:**
  - RTC_CNTL_PLL_BUF_WAIT
  - RTC_CNTL_XTL_BUF_WAIT
  - RTC_CNTL_CPUSTALL_EN
  - RTC_CNTL_CPUSTALL_WAIT
  - RTC_CNTL_CK8M_WAIT
  - RTC_CNTL_XTL_BUF_WAIT
  - RTC_CNTL_PLL_BUF_WAIT

**Text Descriptions:**
- **RTC_CNTL_CPUSTALL_EN:** Enables CPU stalling. (R/W)
- **RTC_CNTL_CPUSTALL_WAIT:** Sets the CPU stall waiting cycle (using the RTC fast clock). (R/W)
- **RTC_CNTL_CK8M_WAIT:** Sets the FOSC waiting cycle (using the RTC slow clock). (R/W)
- **RTC_CNTL_XTL_BUF_WAIT:** Sets the XIAL waiting cycle (using the RTC slow clock). (R/W)
- **RTC_CNTL_PLL_BUF_WAIT:** Sets the PLL waiting cycle (using the RTC slow clock). (R/W)

**Section Header:**
Register 10.9. RTC_CNTL_RTC_TIMER2_REG (0x020)

**Table Description for Register 10.9:**
- **Columns:** Bits, Values in hexadecimal.
- **Rows:**
  - RTC_CNTL_MIN_TIME_CK8M_OFF
  - RTC_CNTL_ULPCP_TOUCH_START_WAIT

**Text Descriptions:**
- **RTC_CNTL_ULPCP TOUCH START WAIT:** Sets the waiting cycle (using the RTC slow clock) before the ULP co-processor starts to work. (R/W)
- **RTC_CNTL_MIN TIME CK8M OFF:** Sets the minimal cycle for FOSC clock (using the RTC slow clock) when powered down. (R/W)

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)
Page number at bottom center of page is "591".