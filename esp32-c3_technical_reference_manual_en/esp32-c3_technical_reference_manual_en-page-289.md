

```markdown
Figure 11.2-1 is a diagram of timer TO in a timer group. TO contains a clock selector, a 16-bit integer divider as a prescaler, a timer-based counter and a comparator for alarm generation.

## 11.2 Functional Description

### 11.2.1 16-bit Prescaler and Clock Selection

The timer can select between the APB clock (APB_CLK) or external clock (XTAL_CLK) as its clock source by setting the TIMG_TO_USE_XTAL field of the TIMG_TOCONFIG_REG register. The selected clock is switched on by setting TIMG_TIMER_CLK_IS_ACTIVE field of the TIMG_REGCLK_REG register to 1 and switched off by setting it to 0. The clock is then divided by a 16-bit prescaler to generate the time-base counter clock (TB_CLK) used by the time-base counter. When the TIMG_TO_DIVIDER field is configured as 2 ~ 65536, the divisor of the prescaler would be 2 ~ 65536. Note that programming value 0 to TIMG_TO_DIVIDER will result in the divisor being 65536. When the TIMG_TO_DIVIDER is set to 1, the actual divisor is 2 so the timer counter value represents half of real time.

To modify the 16-bit prescaler, please first configure the TIMG_TO_DIVIDER field, and then set TIMG_TO_DIVIDER_RST to 1. Meanwhile, the timer must be disabled (i.e. TIMG_TO_EN should be cleared). Otherwise, the result can be unpredictable.

### 11.2.2 54-bit Time-base Counter

The 54-bit time-base counters are based on TB_CLK and can be configured to increment or decrement via the TIMG_TO_INCREASE field. The time-base counter can be enabled or disabled by setting or clearing the TIMG_TO_EN field, respectively. When enabled, the time-base counter increments or decrements on each cycle of TB_CLK. When disabled, the time-base counter is essentially frozen. Note that the TIMG_TO_INCREASE field can be changed while TIMG_TO_EN is set and this will cause the time-base counter to change direction instantly.

To read the 54-bit value of the time-base counter, the timer value must be latched to two registers before being read by the CPU (due to the CPU being 32-bit). By writing any value to the TIMG_TOUPDATE_REG, the current value of the 54-bit timer starts to be latched into the TIMG_TOLO_REG and TIMG_TOHI_REG registers containing the lower 32-bits and higher 22-bits, respectively. When TIMG_TOUPDATE_REG is cleared by hardware, it indicates the latch operation has been completed and current timer value can be read from the TIMG_TOLO_REG and TIMG_TOHI_REG registers. TIMG_TOLO_REG and TIMG_TOHI_REG registers will remain unchanged for the CPU to read in its own time until TIMG_TOUPDATE_REG is written to again.
```