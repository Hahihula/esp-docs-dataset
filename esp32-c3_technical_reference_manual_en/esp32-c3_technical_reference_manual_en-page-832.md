

```markdown
Chapter 32 LED PWM Controller (LEDC)  GoBack


The bits `LEDC_DUTY_CHn[3:0]` are used to dither the duty cycles of the PWM output signal (`sig_outn`) by periodically altering the duty cycle of `sig_outn`. When `LEDC_DUTY_CHn[3:0]` is set to a non-zero value, then for every 16 cycles of `sig_outn`, `LEDC_DUTY_CHn[3:0]` of those cycles will have PWM pulses that are one timer tick longer than the other (`(16 - LEDC_DUTY_CHn[3:0])` cycles). For instance, if `LEDC_DUTY_CHn[18:4]` is set to 10 and `LEDC_DUTY_CHn[3:0]` is set to 5, then 5 of 16 cycles will have a PWM pulse with a duty value of 11 and the rest of the 16 cycles will have a PWM pulse with a duty value of 10. The average duty cycle after 16 cycles is 10.3125.

If fields `LEDC_TIMER_SEL_CHn`, `LEDC_HPOINT_CHn`, `LEDC_DUTY_CHn[18:4]` and `LEDC_SIG_OUT_EN_CHn` are reconfigured, `LEDC_PARA_UP_CHn` must be set to apply the new configuration. This will cause the newly configured values to take effect upon the next overflow of the counter. `LEDC_PARA_UP_CHn` field will be automatically cleared by hardware.


32.3.4 Duty Cycle Fading

The PWM generators can fade the duty cycle of a PWM output signal (i.e. gradually change the duty cycle from one value to another). If Duty Cycle Fading is enabled, the value of `Lpointn` will be incremented/decremented after a fixed number of counter overflows has occurred. Figure 32.3-4 illustrates Duty Cycle Fading.

Duty Cycle Fading is configured using the following register fields:

*   `LEDC_DUTY_CHn` is used to set the initial value of `Lpointn`.
```