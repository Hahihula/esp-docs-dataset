
```markdown
## 41.3.2 PWM Timer Module

MCPWM has three PWM timer modules. Any of them can determine the necessary event timing for any of the three PWM operator modules. By using the synchronization signals from the GPIO matrix, built-in synchronization logic allows multiple PWM timer modules in one or more MCPWM peripherals to work together as a system.

### 41.3.2.1 Configurations of the PWM Timer Module

Users can configure the following functions of the PWM timer module:

*   Control how often events occur by specifying the PWM timer frequency or period.
*   Configure a particular PWM timer to synchronize phases with other PWM timers or modules.
*   Configure the following timer counting modes: count-up, count-down, count-up-down.
*   Change the rate of the PWM timer clock (PT_CLK) with a prescaler. Each timer has its own prescaler configured with `MCPWM_TIMERn_PRESCALE` of the register `MCPWM_TIMER0_CFG0_REG`. The PWM timer increments or decrements at a slower pace, depending on the setting of this field. The new `MCPWM_TIMERn_PRESCALE` configuration value will take effect when the timer stops and starts counting again.

### 41.3.2.2 PWM Timer's Working Modes and Timing Event Generation

The PWM timer has three working modes, selected by the `PWMx_timer mode` field:

*   **Count-Up Mode:**
    The PWM timer increments from zero until reaching the value configured in the period field. Once done, the PWM timer returns to zero and starts increasing again. PWM period = the value of the period field + 1.
    Note: The period field is `MCPWM_TIMERn_PERIOD` (x = 0, 1, 2), i.e., `MCPWM_TIMERO_PERIOD`, `MCPWM_TIMER1_PERIOD`, `MCPWM_TIMER2_PERIOD`.

*   **Count-Down Mode:**
    The PWM timer decrements to zero, starting from the value configured in the period field. Once done, the PWM timer returns to the period value and starts decrementing again. In this case, the PWM period = the value of period field + 1.

*   **Count-Up-Down Mode:**
    This is a combination of the two modes mentioned above. The PWM timer starts increasing from zero until the period value is reached. Then, the timer decreases back to zero. The PWM timer cycles incrementally and decrementally in this mode. The PWM period = the value of the period field × 2.

Figures 41.3-5 to 41.3-8 show PWM timer waveforms in different modes, including timer behavior during synchronization events. In Count-Up mode, the counting direction after synchronization is always counting up. In Count-Down mode, the counting direction after synchronization is always counting down. In Count-Up-Down Mode, the counting direction after synchronization can be chosen by setting the `MCPWM_TIMERn_PHASE_DIRECTION`.
```