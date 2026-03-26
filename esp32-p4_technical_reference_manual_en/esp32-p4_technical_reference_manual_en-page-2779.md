

```markdown
- If Timerx_cnt == Hpointn, sig_outn is 1.
- If Timerx_cnt == Lpointn, sig_outn is 0.

Figure 55.4-3 illustrates how Hpointn and Lpointn are used to generate a fixed duty cycle PWM output signal.

![Figure 55.4-3. LED PWM Output Signal Diagram](image)

For a particular PWM generator (PWMn), its Hpointn is sampled from the `LEDC_HPOINT_CHn` field each time the selected timer’s counter overflows. Likewise, Lpointn is also sampled on every counter overflow and is calculated from the sum of the `LEDC_DUTY_CHn[24:4]` and `LEDC_HPOINT_CHn` fields. By setting Hpointn and Lpointn via the `LEDC_HPOINT_CHn` and `LEDC_DUTY_CHn[24:4]` fields, the relative phase and duty cycle of the PWM output can be set.

The PWM output signal (sig_outn) is enabled by setting `LEDC_SIG_OUT_EN_CHn`. When `LEDC_SIG_OUT_EN_CHn` is cleared, PWM signal output is disabled, and the output signal (sig_outn) will output a constant level specified by `LEDC_IDLE_LV_CHn`.

The bits `LEDC_DUTY_CHn[3:0]` are used to dither the duty cycles of the PWM output signal (sig_outn) by periodically altering the duty cycle of sig_outn. When `LEDC_DUTY_CHn[3:0]` is not 0, then for every 16 cycles of sig_outn, `LEDC_DUTY_CHn[3:0]` of those cycles will have PWM pulses that are one timer tick longer than the other (16- `LEDC_DUTY_CHn[3:0]`) cycles. For instance, if `LEDC_DUTY_CHn[24:4]` is set to 10 and `LEDC_DUTY_CHn[3:0]` is set to 5, then 5 of 16 cycles will have a PWM pulse with a duty value of 11 and the rest of the 16 cycles will have a PWM pulse with a duty value of 10. The average duty cycle after 16 cycles is 10.3125.

If fields `LEDC_TIMER_SEL_CHn`, `LEDC_HPOINT_CHn`, `LEDC_DUTY_CHn[24:4]`, and `LEDC_SIG_OUT_EN_CHn` are reconfigured, `LEDC_PARA_UP_CHn` must be set to apply the new configuration. This will cause the newly configured values to take effect upon the next overflow of the counter. `LEDC_PARA_UP_CHn` field will be automatically cleared by hardware.

## 55.4.3 Duty Cycle Fading

The PWM generators can fade the duty cycle of a PWM output signal (i.e., gradually change the duty cycle from one value to another). Each PWM generator can have up to 16 duty cycle ranges, which can be independently configured in terms of fading direction (increase or decrease), fading amount, the number of fades, and fading frequency. If Duty Cycle Fading is enabled, every range’s Lpointn value will change
```