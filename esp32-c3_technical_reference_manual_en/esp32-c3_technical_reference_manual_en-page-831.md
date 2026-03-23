

```markdown
Table 32.3-1. Commonly-used Frequencies and Resolutions

| LEDC_CLKx | PWM Frequency | Highest Resolution (bit)¹ | Lowest Resolution (bit)² |
|-----------|---------------|---------------------------|--------------------------|
| RC_FAST_CLK (17.5 MHz) | 1 kHz         | 14                        | 5                        |
| RC_FAST_CLK (17.5 MHz) | 1.75 kHz      | 13                        | 4                        |

¹ The highest resolution is calculated when the clock divisor LEDC_CLK_DIV is 1 and rounded down. If the highest resolution calculated by the formula is higher than the counter’s width 14 bits, then the highest resolution should be 14 bits.
² The lowest resolution is calculated when the clock divisor LEDC_CLK_DIV is 1023 + 255/256 and rounded up. If the lowest resolution calculated by the formula is lower than 0, then the lowest resolution should be 1.

To change the overflow value at runtime, first set the `LEDC_TIMERx_DUTY_RES` field, and then set the `LEDC_TIMERx_PARA_UP` field. This will cause the newly configured values to take effect upon the next overflow of the counter. If `LEDC_OVF_CNT_EN_CHn` field is reconfigured, `LEDC_PARA_UP_CHn` should be set to apply the new configuration. In summary, these configuration values need to be updated by setting `LEDC_TIMERx_PARA_UP` or `LEDC_PARA_UP_CHn`. `LEDC_TIMERx_PARA_UP` and `LEDC_PARA_UP_CHn` will be automatically cleared by hardware.

32.3.3 PWM Generators

To generate a PWM signal, a PWM generator (PWMn) selects a timer (Timerx). Each PWM generator can be configured separately by setting `LEDC_TIMER_SEL_CHn` to use one of four timers to generate the PWM output.

As shown in Figure 32.3-1, each PWM generator has a comparator and two multiplexers. A PWM generator compares the timer’s 14-bit counter value (`Timerx_cnt`) to two trigger values `Hpointn` and `Lpointn`. When the timer’s counter value is equal to `Hpointn` or `Lpointn`, the PWM signal is high or low, respectively, as described below:

- If `Timerx_cnt == Hpointn`, `sig_outn` is 1.
- If `Timerx_cnt == Lpointn`, `sig_outn` is 0.

Figure 32.3-3 illustrates how `Hpointn` or `Lpointn` are used to generate a fixed duty cycle PWM output signal.

For a particular PWM generator (PWMn), its `Hpointn` is sampled from the `LEDC_HPOINT_CHn` field each time the selected timer’s counter overflows. Likewise, `Lpointn` is also sampled on every counter overflow and is calculated from the sum of the `LEDC_DUTY_CHn[18:4]` and `LEDC_HPOINT_CHn` fields. By setting `Hpointn` and `Lpointn` via the `LEDC_HPOINT_CHn` and `LEDC_DUTY_CHn[18:4]` fields, the relative phase and duty cycle of the PWM output can be set.

The PWM output signal (`sig_outn`) is enabled by setting `LEDC_SIG_OUT_EN_CHn`. When `LEDC_SIG_OUT_EN_CHn` is cleared, PWM signal output is disabled, and the output signal (`sig_outn`) will output a constant level as specified by `LEDC_IDLE_LV_CHn`.
```