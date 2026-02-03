**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Header:**
Register 36.14. MCPWM_TIMER_SYNCI_CFG_REG (0x0034)

**Binary Diagram Description:**
- The diagram shows a binary representation of the register with labels for each bit position from least significant to most significant.

**Subtitles and Lists under "MCPWM_TIMERO_SYNCISCEL":**

- **Select sync input for PWM timer0. (R/W)**
  - 1: PWM timer0 sync_out;
  - 2: PWM timer1 sync_out;
  - 3: PWM timer2 sync_out;
  - 4: SYNCO from GPIO matrix;
  - 5: SYNC1 from GPIO matrix;
  - 6: SYNC2 from GPIO matrix;

- **Other values:** no sync input selected.

**Subtitles and Lists under "MCPWM_TIMER1_SYNCISCEL":**

- **Select sync input for PWM timer1. (R/W)**
  - 1: PWM timer0 sync_out;
  - 2: PWM timer1 sync_out;
  - 3: PWM timer2 sync_out;
  - 4: SYNCO from GPIO matrix;
  - 5: SYNC1 from GPIO matrix;
  - 6: SYNC2 from GPIO matrix;

- **Other values:** no sync input selected.

**Footer Note:**
Continued on the next page...

**Document Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback