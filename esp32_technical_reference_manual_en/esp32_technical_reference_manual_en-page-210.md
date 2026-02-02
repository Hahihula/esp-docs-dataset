**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Header:**
Register 9.24. RTC_CNTL_CLK_CONF_REG (0x070)

**Table Description:**
The table lists various configuration registers related to the Real-Time Clock Control Register, including their bit positions and descriptions.

- **Columns:** 
  - Bit Positions
  - Register Name

- **Rows:**
  - RTC_CNTL_ANA_CLK_RTC_SEL
  - RTC_CNTL_SLOW_CLK_sel.
  - RTC_CNTL_4K8M_EN
  - RTC_CNTL_D32K_EN
  - RTC_CNTL_64K8M_EN
  - RTC_CNTL_128K8M_EN
  - RTC_CNTL_256K8M_EN
  - RTC_CNTL_512K8M_EN

**Text:**
- RTC_CNTL_ANA_CLK_RTC_SEL: RTC_SLOW_CLK sel. 0: RC_SLOW_CLK, 1: XTL32K_CLK.
- RTC_CNTL_4K8M_EN (R/W): Enable 4K8M for digital core
- RTC_CNTL_SLOW_CLK_sel.: XTAL div 4; 1: CK8M.

**Additional Configuration Details:**
- RTC_CNTL_SOC_CLK_SEL:
  - 0: XTAL, 1: PLL, 2: CK8M, 3: APLL.
- RTC_CNTL_64K8M_EN (R/W): Enable RC_FAST_DIV_CLK for digital core
- RTC_CNTL_128K8M_EN (R/W): Enable RC_SLOW_DIV_CLK

**Divider Information:**
- RTC_CNTL_Divider = reg_rtc_cntl_ck8m_div_sel + 1.
- RTC_CNTL_DIG_CLK8M_EN:
  - Enables CK8M for digital core
- RTC_CNTL_ENB_4K8M_DIV (R/W): Enable 4K8M for clock division

**Miscellaneous:**
- RTC_CNTL_DIG_XTAL32K_EN enables XTAL32K for the digital core.
- RTC_CNTL_ENB_64K8M_DIV:
  - RC_FAST_DIV_CLK is actually CK8M divided by 256.

**Footer Information:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:** 
210