**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Heading:**
GoBack

**Body Text with Subsections and Lists:**

- Change the rate of the PWM timer clock (PTyclk) with a prescaler. Each timer has its own prescaler configured with `MCPWM_TIMERx_PRESCALE` of the register `MCPWM_TIMERO_CFGO_REG`. The PWM timer increments or decrements at a slower pace, depending on the setting of this field.

**Subsection Title:**
36.3.2.2 PWM Timer’s Working Modes and Timing Event Generation

- **Count-Up Mode:**  
  In this mode, the PWM timer increments from zero until reaching the value configured in the period field. Once done, the PWM timer returns to zero and starts increasing again. PWM period is equal to the value of the period field + 1.
  - Note: The period field is `MCPWM_TIMERx_PERIOD` (x = 0, 1, 2), i.e., `MCPWM_TIMERO_PERIOD`, `MCPWM_TIMER1_PERIOD`, or `MCPWM_TIMER2_PERIOD`.

- **Count-Down Mode:**  
  The PWM timer decrements to zero, starting from the value configured in the period field. After reaching zero, it is set back to the period value. Then it starts to decrement again. In this case, the PWM period is also equal to the value of period field + 1.

- **Count-Up-Down Mode:**  
  This is a combination of the two modes mentioned above. The PWM timer starts increasing from zero until the period value is reached. When then, the timer decreases back to zero. This pattern is repeated.
  - Note: The PWM period is calculated as (the value of the period field × 2 + 1).

**Additional Information:**  
Figures `36.3-6` and `36.3-9` show PWM timer waveforms in different modes, including timer behavior during synchronization events.

In Count-Up mode:
- The counting direction after synchronization is always increasing.
- In Figure: `PWM Timer 0xFFFFF`
- Description of the waveform with period setting at zero crossing from high to low and back up again. 

In Count-Down Mode:

**Figure Caption:**  
Figure 36.3-6. Count-Up Mode Waveform

**Footer Information:**
Espressif Systems
1333 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback