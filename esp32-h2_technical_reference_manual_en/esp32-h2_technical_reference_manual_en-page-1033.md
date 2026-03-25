
```markdown
4. Set `LEDC_OVF_CNT_CHn_INT_ENA` to enable the overflow interrupt  
5. Set `LEDC_TIMERx_DUTY_RES` to enable the timer and wait for a `LEDC_OVF_CNT_CHn_INT` interrupt  

To change the overflow value at runtime, first set the `LEDC_TIMERx_DUTY_RES` field, and then set the `LEDC_TIMERx_PARA_UP` field. This will cause the newly configured values to take effect upon the next overflow of the counter. If `LEDC_OVF_CNT_EN_CHn` field is reconfigured, `LEDC_PARA_UP_CHn` should be set to apply the new configuration. In summary, these configuration values need to be updated by setting `LEDC_TIMERx_PARA_UP` or `LEDC_PARA_UP_CHn`. `LEDC_TIMERx_PARA_UP` and `LEDC_PARA_UP_CHn` will be automatically cleared by hardware.

Referring to Figure 35.3-1, the frequency of a PWM generator output signal (`sig_outn`) is dependent on the frequency of the timer’s clock source `LEDC_CLKx`, the clock divisor `LEDC_CLK_DIV`, and the duty resolution (counter width) `LEDC_TIMERx_DUTY_RES`:

$$f_{PWM} = \frac{f_{LEDC\_CLKx}}{LEDC\_CLK\_DIV \times 2^{LEDC\_TIMERx\_DUTY\_RES}}$$

Based on the formula above, the desired duty resolution can be calculated as follows:

$$LEDC\_TIMERx\_DUTY\_RES = \log_2\left(\frac{f_{LEDC\_CLKx}}{f_{PWM} \cdot LEDC\_CLK\_DIV}\right)$$

Table 35.3-1 lists the commonly-used frequencies and their corresponding resolutions.

**Table 35.3-1. Commonly-used Frequencies and Resolutions**

| `LEDC_CLKx` | PWM Frequency | Highest Resolution (bit)¹ | Lowest Resolution (bit)² |
|-------------|---------------|---------------------------|--------------------------|
| PLL_F96M_CLK (96 MHz) | 1 kHz | 17 | 6 |
| PLL_F96M_CLK (96 MHz) | 5 kHz | 15 | 4 |
| PLL_F96M_CLK (96 MHz) | 10 kHz | 14 | 3 |
| XTAL_CLK (32 MHz) | 1 kHz | 15 | 4 |
| XTAL_CLK (32 MHz) | 4 kHz | 13 | 2 |
| RC_FAST_CLK (8 MHz) | 1 kHz | 13 | 2 |
| RC_FAST_CLK (8 MHz) | 2 kHz | 12 | 1 |

¹ The highest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is 1. If the highest resolution calculated by the formula is higher than the counter’s width 20 bits, then the highest resolution should be 20 bits.  
² The lowest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is $1023 + \frac{255}{256}$. If the lowest resolution calculated by the formula is lower than 0, then the lowest resolution should be 1.

## 35.3.3 PWM Generators

To generate a PWM signal, a PWM generator (`PWMn`) needs a timer (`Timerx`). Each PWM generator can be configured separately by setting `LEDC_TIMER_SEL_CHn` to use one of four timers to generate the PWM output.
```