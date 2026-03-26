

```markdown
Figure 55.4-1 illustrates the relation between LEDC_CLK clock pulses and ref_pulsex clock pulses when LEDC_CLK_DIV is a non-integer value.

Figure 55.4-1. Frequency Division When LEDC_CLK_DIV is a Non-Integer Value

To change the timer's clock divisor at runtime, first configure the `LEDC_CLK_DIV_TIMERx` field, and then set the `LEDC_TIMERx_PARA_UP` field to apply the new configuration. This will cause the newly configured values to take effect upon the next overflow of the counter. The `LEDC_TIMERx_PARA_UP` field will be automatically cleared by hardware.

55.4.1.3 20-Bit Counter

Each timer contains a 20-bit timebase counter that uses ref_pulsex as its reference clock (see Figure 55.3-2). The `LEDC_TIMERx_DUTY_RES` field configures the actual used bit width of this 20-bit counter. Hence, the maximum resolution of the PWM signal is 20 bits. The counter counts up to `2^LEDC_TIMERx_DUTY_RES - 1`, overflows and begins counting from 0 again. The counter's value can be read, reset, and suspended by software.

Figure 55.4-2 shows the relationship between the counter and PWM resolution.

Figure 55.4-2. Relationship Between Counter And Resolution

Every time the counter overflows, it can trigger the `LEDC_TIMERx_OVF_INT` interrupt (generated automatically by hardware without configuration). It can also be configured to trigger `LEDC_OVF_CNT_CHn_INT` interrupt after overflowing `LEDC_OVF_NUM_CHn + 1` times. To configure `LEDC_OVF_CNT_CHn_INT` interrupt, please:

1. Configure `LEDC_TIMER_SEL_CHn` to select the timer for the PWM generator
2. Enable the overflow counter by setting `LEDC_OVF_CNT_EN_CHn`
3. Configure `LEDC_OVF_NUM_CHn` with the number of counter overflows (that triggers an interrupt) minus 1
4. Enable the overflow interrupt by setting `LEDC_OVF_CNT_CHn_INT_ENA`
5. Configure `LEDC_TIMERx_DUTY_RES` to specify the counter bit width for the selected Timerx and wait for a `LEDC_OVF_CNT_CHn_INT` interrupt
```