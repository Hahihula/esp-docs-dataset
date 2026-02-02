**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Section Header:**
Register 9.19. RTC_CNTL_LOW_POWER_ST_REG (0x00CO)

**Binary Register Diagram Description:**

- **Field Labels and Values:** 
  - RTC_CNTLMainStateInIdle
    - [31, 28] (reserved)
    - [27, 26] (reserved)
    - [25, 24] (reserved)
    - [20, 19] (reserved)
    - [18] (reserved)

- **Field Description:**
  - RTC_CNTL_RTC_RDY_FOR_WAKEUP
    - The value indicates the RTC is ready to be triggered by any wakeup source. (RO) 

**Subsection Title and Field Description:** 
RTC_CNTLMainStateInIdle Indicates the RTC state.
- [0]: the chip can be either in sleep modes, entering sleep modes; wait until RTC_CNTL_RTC_RDY_FOR_WAKEUP bit is set then you can wake up the chip or exiting sleep mode. In this case, RTC_CNTL_MAIN_STATE_IN_IDLE will eventually become 1.

**Binary Register Diagram Description:**

- **Field Labels and Values:** 
  - RTC_CNTL_XTL_EXT_CTR_EN
    - [30] (reserved)
    - [29]
  
- **Field Description:**
  - RTC_CNTL_XTL_EXT_CTR_EN Enable control XTAL with external pads. (R/W)

**Binary Register Diagram Description:**

- **Field Labels and Values:** 
  - RTC_CNTL_XTL_EXT_CTR_LV
    - [31, 29] (reserved)
  
- **Field Description:**
  - RTC_CNTL_XTL_EXT_CTR_LV O: power down XTAL at high level; 1: power down XTAL at low level. (R/W)

**Footer Information:** 
Espressif Systems
Page Number: 207
Document Version: ESP32 TRM (Version 5.6)
Submit Documentation Feedback