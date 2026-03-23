

```markdown
To change the timer's clock divisor at runtime, first configure the `LEDC_CLK_DIV_TIMERx` field, and then set the `LEDC_TIMERx_PARA_UP` field to apply the new configuration. This will cause the newly configured values to take effect upon the next overflow of the counter. The `LEDC_TIMERx_PARA_UP` field will be automatically cleared by hardware.

### 32.3.2.3 14-bit Counter

Each timer contains a 14-bit timebase counter that uses `ref_pulsex` as its reference clock (see Figure 32.3-1). The `LEDC_TIMERx_DUTY_RES` field configures the overflow value of this 14-bit counter. Hence, the maximum resolution of the PWM signal is 14 bits. The counter counts up to `2^LEDC_TIMERx_DUTY_RES - 1`, overflows and begins counting from 0 again. The counter's value can be read, reset, and suspended by software.

The counter can trigger `LEDC_TIMERx_OVF_INT` interrupt (generated automatically by hardware without configuration) every time the counter overflows. It can also be configured to trigger `LEDC_OVF_CNT_CHn_INT` interrupt after the counter overflows `LEDC_OVF_NUM_CHn + 1` times. To configure `LEDC_OVF_CNT_CHn_INT` interrupt, please:

1. Configure `LEDC_TIMER_SEL_CHn` as the counter for the PWM generator.
2. Enable the counter by setting `LEDC_OVF_CNT_EN_CHn`.
3. Set `LEDC_OVF_NUM_CHn` to the number of counter overflows to generate an interrupt, minus 1.
4. Enable the overflow interrupt by setting `LEDC_OVF_CNT_CHn_INT_ENA`.
5. Set `LEDC_TIMERx_DUTY_RES` to enable the timer and wait for a `LEDC_OVF_CNT_CHn_INT` interrupt.

Referring to Figure 32.3-1, the frequency of a PWM generator output signal (`sig_outn`) is dependent on the frequency of the timer's clock source `LEDC_CLKx`, the clock divisor `LEDC_CLK_DIV`, and the duty resolution (counter width) `LEDC_TIMERx_DUTY_RES`:

```math
f_{PWM} = \frac{f_{LEDC\_CLKx}}{LEDC\_CLK\_DIV \cdot 2^{LEDC\_TIMERx\_DUTY\_RES}}
```

Based on the formula above, the desired duty resolution can be calculated as follows:

```math
LEDC_TIMERx_DUTY_RES = \log_2\left(\frac{f_{LEDC\_CLKx}}{f_{PWM} \cdot LEDC_CLK\_DIV}\right)
```

Table 32.3-1 lists the commonly-used frequencies and their corresponding resolutions.

**Table 32.3-1. Commonly-used Frequencies and Resolutions**

| `LEDC_CLKx` | PWM Frequency | Highest Resolution (bit)¹ | Lowest Resolution (bit)² |
|-------------|---------------|---------------------------|--------------------------|
| APB_CLK (80 MHz) | 1 kHz | 14 | 7 |
| APB_CLK (80 MHz) | 5 kHz | 13 | 4 |
| APB_CLK (80 MHz) | 10 kHz | 12 | 3 |
| XTAL_CLK (40 MHz) | 1 kHz | 14 | 6 |
| XTAL_CLK (40 MHz) | 4 kHz | 13 | 4 |

---

¹ The highest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is 1 and rounded down. If the highest resolution calculated by the formula is higher than the counter's width 14 bits, then the highest resolution should be 14 bits.

² The lowest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is `1023 + 255/256` and rounded up. If the lowest resolution calculated by the formula is lower than 0, then the lowest resolution should be 1.
```