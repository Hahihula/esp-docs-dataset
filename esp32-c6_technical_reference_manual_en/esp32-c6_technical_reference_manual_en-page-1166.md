

```markdown
Chapter 35 LED PWM Controller (LEDC)

- The ref_pulseX clock pulses generated every (A+1) pulses are evenly distributed amongst those generated every A pulses

Figure 35.3-2 illustrates the relation between LEDC_CLKx clock pulses and ref_pulseX clock pulses when LEDC_CLK_DIV is a non-integer value.

![Figure 35.3-2: Frequency Division When LEDC_CLK_DIV is a Non-Integer Value](image)

To change the timer's clock divisor at runtime, first configure the `LEDC_CLK_DIV_TIMERx` field, and then set the `LEDC_TIMERx_PARA_UP` field to apply the new configuration. This will cause the newly configured values to take effect upon the next overflow of the counter. The `LEDC_TIMERx_PARA_UP` field will be automatically cleared by hardware.

35.3.2.3 20-Bit Counter

Each timer contains a 20-bit timebase counter that uses ref_pulseX as its reference clock (see Figure 35.3-1). The `LEDC_TIMERx_DUTY_RES` field configures the overflow value of this 20-bit counter. Hence, the maximum resolution of the PWM signal is 20 bits. The counter counts up to `2^LEDC_TIMERx_DUTY_RES - 1`, overflows and begins counting from 0 again. The counter's value can be read, reset, and suspended by software. Figure 35.3-3 shows the relationship between the counter and PWM resolution.

![Figure 35.3-3: Relationship Between Counter And Resolution](image)

Every time the counter overflows, it can trigger the `LEDC_TIMERx_OVF_INT` interrupt (generated automatically by hardware without configuration). It can also be configured to trigger `LEDC_OVF_CNT_CHn_INT` interrupt after overflowing `LEDC_OVF_NUM_CHn + 1` times. To configure `LEDC_OVF_CNT_CHn_INT` interrupt, please:

1. Configure `LEDC_TIMER_SEL_CHn` to select the timer for the PWM generator
2. Enable the overflow counter by setting `LEDC_OVF_CNT_EN_CHn`
3. Configure `LEDC_OVF_NUM_CHn` with the number of counter overflows (that triggers an interrupt) minus 1
4. Enable the overflow interrupt by setting `LEDC_OVF_CNT_CHn_INT_ENA`

Espressif Systems    1166
ESP32-C6 TRM (Version 1.1)
```