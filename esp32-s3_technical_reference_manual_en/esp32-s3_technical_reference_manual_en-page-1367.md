**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 36.6. MCPWM_TIMER1_CFGO_REG (0x014)

**Table Description for Register 36.6:**
- **Columns**: 
  - Bit positions from most significant bit to least significant bit.
  - Values range is shown as "0" and "Reset".
  
- **Rows**:
  - MCPWM_TIMER1_PRESCALE
    - Description: Period of PTO_clk = Period of PWM_clk * (PWM_timer1_PRESCALE + 1). 
      - Access type: Read/Write
  
  - MCPWM_TIMER1_PERIOD
    - Description: Period shadow register of PWM timer1. 
      - Access type: Read/Write

  - MCPWM_TIMER1_PERIOD_UPMETHOD
    - Description: Update method for active register of PWM timer1 period, with different methods (0: immediate, 1: TEZ, 2: sync, 3: TEZ | sync).
      - Access type: Read/Write
  
**Section Header:**
Register 36.7. MCPWM_TIMER1_CFG1_REG (0x018)

**Table Description for Register 36.7:**
- **Columns**: 
  - Bit positions from most significant bit to least significant bit.
  
- **Rows**:
  - MCPWM_TIMER1_MOD
    - Description: PWM timer1 working mode, with different modes described (0: freeze; 1: increase mode; 2: decrease mode; 3: up-down mode).
      - Access type: Read/Write

---

**Section Header:**
MCPWM_TIMER1_START

- **Description**: PWM timer1 start and stop control.
  - Access type: Read/Write
  - Values:
    - "0": if PWM timer1 starts, then stops at TEZ;
    - "1": if timer1 starts, then stops at TEP;
    - "2": PWM timer1 starts and runs on;
    - "3": timer1 starts and stops at the next TEZ;
    - "4": timer1 starts and stops at the next TEP.

**Section Header:**
TEP here and below means the event that happens when the timer equals to period.
  
---

**Footer Information:** 
Espressif Systems
Page number 1367

**Document Title:** ESP32-S3 TRM (Version 1.7)

**Feedback Link:** Submit Documentation Feedback