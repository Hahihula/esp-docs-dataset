**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Subtitle:**
Register 36.3. MCPWM_TIMERO_CFG1_REG (0x0008)

**Menu/Navigation Link:**
GoBack

**Table Description with Labels and Values:**
- **Columns:** 
  - The first column is labeled "31" at the top.
  - Other columns are not explicitly named but contain binary values.

- **Rows:**
  - All rows consist of a series of zeros (0) except for one row which has all ones (1).

**Section Title and Description:**

**MCPWM_TIMERO_START**
PWM timer0 start and stop control. (R/W/SC)

- O: if PWM timer0 starts, then stops at TEZ;
- 1: if timer0 starts, then stops at TEP;
- 2: PWM timer0 starts and runs on;
- 3: timer0 starts and stops at the next TEZ;
- 4: timer0 starts and stops at the next TEP.

TEP here and below means the event that happens when the timer equals to period.

**MCPWM_TIMERO_MOD**
PWM timer0 working mode. (R/W)

- O: freeze;
- 1: increase mode
- 2: decrease mode.
- 3: up-down mode

**Footer Information:**
Espressif Systems  
Page number and document version:
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback