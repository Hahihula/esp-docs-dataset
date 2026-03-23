

```markdown
5. Set `LEDC_TIMERx_DUTY_RES` to enable the timer and wait for a `LEDC_OVF_CNT_CHn_INT` interrupt

To change the overflow value at runtime, first set the `LEDC_TIMERx_DUTY_RES` field, and then set the `LEDC_TIMERx_PARA_UP` field. This will cause the newly configured values to take effect upon the next overflow of the counter. If `LEDC_OVF_CNT_EN_CHn` field is reconfigured, `LEDC_PARA_UP_CHn` should be set to apply the new configuration. In summary, these configuration values need to be updated by setting `LEDC_TIMERx_PARA_UP` or `LEDC_PARA_UP_CHn`. `LEDC_TIMERx_PARA_UP` and `LEDC_PARA_UP_CHn` will be automatically cleared by hardware.

Referring to Figure 35.3-1, the frequency of a PWM generator output signal (`sig_outn`) is dependent on the frequency of the timer’s clock source `LEDC_CLKx`, the clock divisor `LEDC_CLK_DIV`, and the duty resolution (counter width) `LEDC_TIMERx_DUTY_RES`:

```math
f_{PWM} = \frac{f_{LEDC\_CLKx}}{LEDC\_CLK\_DIV \cdot 2^{LEDC\_TIMERx\_DUTY\_RES}}
```

Based on the formula above, the desired duty resolution can be calculated as follows:

```math
LEDC_TIMERx_DUTY_RES = \log_2\left(\frac{f_{LEDC\_CLKx}}{f_{PWM} \cdot LEDC_CLK_DIV}\right)
```
```