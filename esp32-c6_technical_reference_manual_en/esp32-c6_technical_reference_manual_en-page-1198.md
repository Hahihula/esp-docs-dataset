

```markdown
- Get a PWM timer in phase with other PWM timers or modules.
- Configure the following timer counting modes: count-up, count-down, count-up-down.
- Change the rate of the PWM timer clock (PT_clk) with a prescaler. Each timer has its own prescaler configured with `MCPWM_TIMERx_PRESCALE` of the register `MCPWM_TIMERO_CFGO_REG`. The PWM timer increments or decrements at a slower pace, depending on the setting of this field. The new `MCPWM_TIMERx_PRESCALE` configuration value will take effect when the timer stops and starts counting again.

### 36.3.2.2 PWM Timer's Working Modes and Timing Event Generation

The PWM timer has three working modes, selected by the `PWMx_timer mode field`:

- **Count-Up Mode:**
  The PWM timer increments from zero until reaching the value configured in the period field. Once done, the PWM timer returns to zero and starts increasing again. PWM period = the value of the period field + 1.
  Note: The period field is `MCPWM_TIMERx_PERIOD` (x = 0, 1, 2), i.e., `MCPWM_TIMERO_PERIOD`, `MCPWM_TIMER1_PERIOD`, `MCPWM_TIMER2_PERIOD`.

- **Count-Down Mode:**
  The PWM timer decrements to zero, starting from the value configured in the period field. Once done, the PWM timer returns to the period value and starts decrementing again. In this case, the PWM period = the value of period field + 1.

- **Count-Up-Down Mode:**
  This is a combination of the two modes mentioned above. The PWM timer starts increasing from zero until the period value is reached. Then, the timer decreases back to zero. The PWM timer cycles incrementally and decrementally in this mode. The PWM period = the value of the period field × 2.

Figures 36.3-7 to 36.3-10 show PWM timer waveforms in different modes, including timer behavior during synchronization events. In Count-Up mode, the counting direction after synchronization is always counting up. In Count-down mode, the counting direction after synchronization is always counting down. In Count-Up-Down Mode, the counting direction after synchronization can be chosen by setting the `MCPWM_TIMERx_PHASE_DIRECTION`.
```

![Figure 36.3-7. Count-Up Mode Waveform](image_path)