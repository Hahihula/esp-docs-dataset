**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Register Information for PWM TIMER1 STATUS REG (0x020):**

- **PWM_TIMER1_DIRECTION**: Current direction of the PWM timer1 counter. Values:
  - `0`: increment
  - `1`: decrement
  
- **PWM_TIMER1_VALUE**: Current value of the PWM timer1 counter.

**Register Information for PWM TIMER2 CFGO REG (0x024):**

- **PWM_TIMER2_PERIOD_UPMETH**: Updating method for active register of PWM timer2 period. Values:
  - `0`: update at TEZ immediately
  - `1`: update at sync
  - `3`: update at TEZ or sync

- **PWM_TIMER2_PERIOD**: Period shadow register of PWM timer2.

- **PWM_TIMER2_PRESCALE**: Period of PT2_clk = Period of PWM_clk * (PWM_TIMER2_PRESCALE + 1). Values:
  - `(R/W)`

**Footer Information:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Diagram Descriptions and Labels for Registers:**

- **PWM_TIMER1_DIRECTION**: Diagram showing the direction bit positions.
  
- **PWM_TIMER1_VALUE**: Diagram indicating the value bits.

- **PWM_TIMER2_PERIOD_UPMETH**: Diagram illustrating different update methods with corresponding binary values (0x000FF, 0x000).

- **PWM_TIMER2_PERIOD**: Diagram depicting period shadow register and its bit positions.
  
- **PWM_TIMER2_PRESCALE**: Diagram showing the pre-scale value calculation.