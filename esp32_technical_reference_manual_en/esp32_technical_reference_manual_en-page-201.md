**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Section Header:**
Register 9.11. RTC_CNTL_ANA_CONF_REG (0x0030)

**Binary Register Diagram Description:**
- The diagram shows a binary register with bits labeled from '31' to '0'.
- Each bit is associated with specific functions:
  - `RTC_CNTL_PLL_I2C_PU` at position `[31]`
  - `RTC_CNTL_OGKEN_12C PU` and others follow in sequence.

**Text Descriptions:**
- RTC_CNTL_PLL_I2C_PU: PLL_I2C power up, otherwise power down. (R/W)
- RTC_CNTL_CKGEN_12C_PU: CKGEN_I2C power up, otherwise power down. (R/W)
- RTC_CNTL_RFRX_PBUS PU: RFRX_PBUS power up, otherwise power down. (R/W)
- RTC_CNTL_TXRF_I2C_PU: TXRF_I2C power up, otherwise power down. (R/W)
- RTC_CNTL_PVTMON_PU: PVTMON power up, otherwise power down. (R/W)
- RTC_CNTL_PLLA FORCE_PU: PLLA force power up. (R/W)
- RTC_CNTL_PLLA FORCE_PD: PLLA force power down. (R/W)

**Section Header:**
Register 9.12. RTC_CNTL_RESET_STATE_REG (0x0034)

**Binary Register Diagram Description:**
- The diagram shows a binary register with bits labeled from '31' to '0'.
- Each bit is associated with specific functions:
  - `RTC_CNTL_PROCPU_STAT_VECTOR_SEL` at position `[31]`
  - `RTC_CNTL_APPCPU_STAT_VECTOR_SEL` and others follow in sequence.

**Text Descriptions:**
- RTC_CNTL_PROCPU_STAT_VECTOR_SEL: PRO_CPU state vector selection. (R/W)
- RTC_CNTL_APPCPU_STAT_VECTOR_SEL: APP_CPU state vector selection. (R/W)
- RTC_CNTL_RESET_CAUSE_APPCPU: Reset cause for APP_CPU. (RO)
- RTC_CNTL_RESET_CAUSE_PROCPU: Reset cause for PRO_CPU. (RO)

**Footer Information:**
Espressif Systems
201 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback