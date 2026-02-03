**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.25. RTC_CNTL_RTC_CLK_CONF_REG (0x0074)

**Body Text and Descriptions for Registers:**

- **Continued from the previous page...**
  
  - **RTC_CNTL_CK8M_DFREQ:** CK8M_DFREQ (R/W)
  
  - **RTC_CNTL_CK8M FORCE_PD:** Set this bit to FPD the RC_FAST_CLK clock. (R/W)
  
  - **RTC_CNTL_CK8M FORCE PU:** Set this bit to FPU the RC_FAST_CLK clock. (R/W)
  
  - **RTC_CNTL_XTAL_GLOBAL_FORCE_GATING:** Set this bit to force gating xtal. (R/W)
  
  - **RTC_CNTL_XTAL_GLOBAL FORCE_NOGATING:** Set this bit to force no nogating xtal. (R/W)
  
  - **RTC_CNTL_FAST_CLK_RTC_SEL:** Set this bit to select the RTC fast clock.
    - `0`: XTAL_DIV_CLK
    - `1`: RC_FAST_CLK div n. (R/W)
  
  - **RTC_CNTL_ANA_CLK_RTC_SEL:** Set this bit to select the RTC slow clock:
    - `0`: RC_SLOW_CLK
    - `1`: XTL32K_CLK 2: RC_FAST_DIV_CLK. (R/W)

**Section Header:**
Register 10.26. RTC_CNTL_RTC_SLOW_CLK_CONF_REG (0x0078)

**Body Text and Description for Register:**

- **RTC_CNTL_ANA_CLK_DIV:** Synchronizes the reg_rtc_ana_clk_div bus.
  - Note that you have to invalidate the bus before switching clock, and validate the new clock. (R/W)
  
- **RTC_CNTL_ANA_CLK_DIV:** Set the RC_SLOW_CLK divider.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)