**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Header:**
Register 9.27. RTC_CNTL_PWC_REG (0x0080)

**Menu/Navigation Link:**
GoBack

**Table Description with Labels and Values:**
- The table lists various register settings for the RTC_CNTL_PWC_REG, each associated with specific functions related to power management in low-power modes.
  - **Columns:** Each column represents a bit position (31 down to 0) of the register along with its corresponding function label.

**Bit Labels and Functions:**
- RTC_CNTL_PD_EN
- RTC_CNTL_FORCE_PU
- RTC_CNTL FORCE PD
- RTC_CNTL_SLOWMEM_PD_EN
- RTC_CNTL_SLOWMEMFORCE_PU
- RTC_CNTL_SLOWMEMFORCE_PD
- RTC_CNTL_SLOWMEMFORCE_LPU
- RTC_CNTL_SLOWMEMFORCE_LPDPD
- RTC_CNTL_SLOWMEMFORCE_ISO
- RTC_CNTL_SLOWMEMFORCE_NOISO

**Function Descriptions:**
1. **RTC_CNTL_PD_EN:** Enable power down rtc_peri in sleep.
2. **RTC_CNTL_FORCE_PU:** rtc_peri force power up (R/W)
3. **RTC_CNTL FORCE PD:** rtc_peri force power down
4. **RTC_CNTL_SLOWMEM_PD_EN:** Enable power down RTC memory in sleep.

**Additional Functions:**
- RTC_CNTL_SLOWMEMFORCE_PU, RTC_CNTL_SLOWMEMFORCE_PD, RTC_CNTL_SLOWMEMFORCE_LPU, RTC_CNTL_SLOWMEMFORCE_LPDPD, RTC_CNTL_SLOWMEMFORCE_ISO
  - These functions are related to the control of slow memory power up/down and isolation in low-power modes.

**Other Functions:**
- RTC_CNTL_FASTMEM_PD, RTC_CNTL_FASTMEMFORCE_PU, RTC_CNTL_FASTMEMFORCE_LPDPD, RTC_CNTL_FASTMEMFORCE_ISO, RTC_CNTL_FASTMEMFORCE_NOISO
  - These functions are related to the control of fast memory power up/down and isolation in low-power modes.

**Special Notes:**
- Some registers have specific notes like "1" indicating a special condition or state (e.g., Fast RTC memory low-power mode PD following CPU; O: fast RTC memory low-power mode PD following RTC state machine).

**Footer Information:**
- Page number 213
- Document version ESP32 TRM (Version 5.6)
- Company name Espressif Systems

**Navigation Link at the Bottom of the Page:**
Submit Documentation Feedback