

```markdown
Chapter 55 LED PWM Controller (LEDC)

GoBack

To change the overflow value at runtime, first set the `LEDC_TIMERx_DUTY_RES` field, and then set the `LEDC_TIMERx_PARA_UP` field. This will cause the newly configured values to take effect upon the next overflow of the counter. If `LEDC_OVF_CNT_EN_CHn` field is reconfigured, `LEDC_PARA_UP_CHn` should be set to apply the new configuration. In summary, these configuration values need to be updated by setting `LEDC_TIMERx_PARA_UP` or `LEDC_PARA_UP_CHn`. `LEDC_TIMERx_PARA_UP` and `LEDC_PARA_UP_CHn` will be automatically cleared by hardware.

Referring to Figure 55.3-2, the frequency of a PWM generator output signal (`sig_outn`) is dependent on the frequency of the timer’s clock source `LEDC_CLK`, the clock divisor `LEDC_CLK_DIV`, and the duty resolution (counter width) `LEDC_TIMERx_DUTY_RES`:

$$
f_{PWM} = \frac{f_{LEDC\_CLK}}{LEDC\_CLK\_DIV \cdot 2^{LEDC\_TIMERx\_DUTY\_RES}}
$$

Based on the formula above, the desired duty resolution can be calculated as follows:

$$
LEDC\_TIMERx\_DUTY\_RES = \log_2\left(\frac{f_{LEDC\_CLK}}{f_{PWM} \cdot LEDC\_CLK\_DIV}\right)
$$

Table 55.4-1 lists the commonly-used frequencies and their corresponding resolutions.

Table 55.4-1. Commonly-used Frequencies and Resolutions

| `LEDC_CLK` | PWM Frequency | Highest Resolution (bit)¹ | Lowest Resolution (bit)² |
|------------|---------------|---------------------------|--------------------------|
| REF_80M_CLK (80 MHz) | 1 kHz | 16 | 6 |
| REF_80M_CLK (80 MHz) | 5 kHz | 13 | 3 |
| REF_80M_CLK (80 MHz) | 10 kHz | 12 | 2 |
| XTAL_40M_CLK (40 MHz) | 1 kHz | 15 | 5 |
| XTAL_40M_CLK (40 MHz) | 4 kHz | 13 | 3 |
| FOSC_20M_CLK (20 MHz) | 1 kHz | 14 | 4 |
| FOSC_20M_CLK (20 MHz) | 2 kHz | 13 | 3 |

¹ The highest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is 1. If the highest resolution calculated by the formula is higher than the counter’s width 20 bits, then the highest resolution should be 20 bits.
² The lowest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is $1023 + \frac{255}{256}$. If the lowest resolution calculated by the formula is lower than 0, then the lowest resolution should be 1.

55.4.2 PWM Generators

To generate a PWM signal, a PWM generator (`PWMn`) needs a timer (`Timerx`). Each PWM generator can be configured separately by setting `LEDC_TIMER_SEL_CHn` to use one of four timers to generate the PWM output.

As shown in Figure 55.3-2, each PWM generator has a comparator and two multiplexers. A PWM generator compares the timer’s 20-bit counter value (`Timerx_cnt`) to two trigger values `Hpointn` and `Lpointn`. When the timer’s counter value is equal to `Hpointn` or `Lpointn`, the PWM signal is high or low, respectively, as described below:
```