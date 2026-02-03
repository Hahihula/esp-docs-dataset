**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**GoBack Link:** GoBack

**Section Header:**
Register 10.1. RTC_CNTL_RTC_OPTIONSO_REG (0x0000)

**Continuation Note:**
Continued from the previous page...

**Body Text and Descriptions for Registers:**

- **RTC_CNTL_XTL FORCE_PD**: Set this bit to FPD the crystal oscillator. (R/W)
  
- **RTC_CNTL_XTL FORCE_PU**: Set this bit to FPU the crystal oscillator. (R/W)

- **RTC_CNTL_DG_WRAPFORCE_RST**: Set this bit to force reset the digital system in deep-sleep.
  - **(R/W)**

- **RTC_CNTL_DG_WRAPFORCE_NORST**: Set this bit to disable force reset to digital system in deep-sleep.
  - (R/W)

- **RTC_CNTL_SW_SYS_RST**: Set this bit to reset the system via SW. (WO)

**Section Header:**
Register 10.2. RTC_CNTL_RTC_SLP_TIMERO_REG (0x0004)

**Body Text and Description for Register:**

- **RTC_CNTL_SLP_VAL_LO**: Sets the lower 32 bits of the trigger threshold for the RTC timer.
  - (R/W)
  
**Register Diagram:** 
- A diagram showing a register with fields labeled "RTC_CNTL_SLP_VAL_LO" at address `0x0000`.

**Section Header:**
Register 10.3. RTC_CNTL_RTC_SLP_TIMER1_REG (0x0008)

**Body Text and Descriptions for Registers:**

- **RTC_CNTL_SLP_VAL_HI**: Sets the higher 16 bits of the trigger threshold for the RTC timer.
  - (R/W)
  
- **RTC_CNTL_RTC_MAIN_TIMER_ALARM_EN**: Sets this bit to enable the timer alarm. 
  - (WO)

**Register Diagram:** 
- A diagram showing a register with fields labeled "RTC_CNTL_SLP_VAL_HI" and "RTC_CNTL_RTCMainTimer_Alarm_EN".
  - The address `0x0008` is indicated.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)