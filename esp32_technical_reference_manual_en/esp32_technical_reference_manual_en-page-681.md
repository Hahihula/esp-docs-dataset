**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Titles and Content:**

1. **Register 29.3. PWM_TIMERO_CFG1_REG (0x0008)**
   - **Field Description:** 
     - `PWM_TIMERO_MOD`: PWM timer0 working mode.
       - Values:
         - `3`: up-down mode, read/write
     - `PWM_TIMERO_START`: PWM timer0 start and stop control.
       - Values:
         - `TEZ`: 1: if timer0 starts, then stops at TEP; 2: PWM timer0 starts and runs on;
         - `4`: timer0 starts and stops at the next TEP. TEP here means when the event that happens to the period.

2. **Register 29.4. PWM_TIMERO_SYNC_REG (0x000c)**
   - **Field Description:**
     - `PWM_TIMERO_PHASE_DIR`: Phase for timer reload.
       - Values:
         - `O`: increase; `1`: decrease, read/write
     - `PWM_TIMERO_PHASE`: Phase for timer reload at sync event. Read/write

3. **Additional Fields in Register 29.4:**
   - `PWM_TIMERO_SYNC_SEL`: PWM timer0 sync_out selection.
     - Values:
       - `O`: sync_in; `1`: TEZ; `2`: TEP
   - `PWM_TIMER1_SYNC_SW`: Trigger a software sync when this bit is toggled, read/write

4. **Field Description:**
   - `PWM_TIMERO_SYNCI_EN`: When set, timer reloading with phase on sync input event.
     - Read/write (R/W)

**Footer Information:** 
- Page number 681
- Document version ESP32 TRM (Version 5.6)
- Company name Espressif Systems

**Navigation Links:**
- Submit Documentation Feedback