**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Menu:**
GoBack

**Subtitle:**
Register 36.10. MCPWM_TIMER2_CFGO_REG (0x0024)

**Diagram Description:**
- The diagram shows a register layout with labels for different bits and their corresponding values.
- Labels include:
  - `MCPWM_TIMER2_PRESCALE`
  - `MCPWM_TIMER2_PERIOD_UPMETHOD`
  - `MCPWM_TIMER2_PERIOD`
  - `MCPWM_TIMER2_PRESCALE` (reserved)
- Bits are numbered from 31 to 0, with some bits labeled as "reserved."

**Text Descriptions:**
- **MCPWM_TIMER2_PRESCAL**: Period of PTO_clk = Period of PWM_clk * (PWM_timer2_PRESCALE + 1). (R/W)

- **MCPWM_TIMER2_PERIOD**: Period shadow register of PWM timer2. (R/W)

- **MCPWM_TIMER2_PERIOD_UPMETHOD**: Update method for active register of PWM timer2 period.
  - `0`: immediate;
  - `1`: TEZ; 
  - `2`: sync; 
  - `3`: TEZ | sync. TEZ here and below means timer equal zero event.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** ESP32-S3 TRM (Version 1.7)