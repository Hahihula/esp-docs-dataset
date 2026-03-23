

```markdown
Chapter 32 LED PWM Controller (LEDC)

- `LEDC_DUTY_START_CHn` will enable/disable duty cycle fading when set/cleared.
- `LEDC_DUTY_CYCLE_CHn` sets the number of counter overflow cycles for every Lpointn increment/decrement. In other words, Lpointn will be incremented/decremented after `LEDC_DUTY_CYCLE_CHn` counter overflows.
- `LEDC_DUTY_INC_CHn` configures whether Lpointn is incremented/decremented if set/cleared.
- `LEDC_DUTY_SCALE_CHn` sets the amount that Lpointn is incremented/decremented.
- `LEDC_DUTY_NUM_CHn` sets the maximum number of increments/decrements before duty cycle fading stops.

If the fields `LEDC_DUTY_CHn`, `LEDC_DUTY_START_CHn`, `LEDC_DUTY_CYCLE_CHn`, `LEDC_DUTY_INC_CHn`, `LEDC_DUTY_SCALE_CHn`, and `LEDC_DUTY_NUM_CHn` are reconfigured, `LEDC_PARA_UP_CHn` must be set to apply the new configuration. After this field is set, the values for duty cycle fading will take effect at once. `LEDC_PARA_UP_CHn` field will be automatically cleared by hardware.

32.3.5 Interrupts

- `LEDC_OVF_CNT_CHn_INT`: Triggered when the timer counter overflows for (`LEDC_OVF_NUM_CHn + 1`) times and the register `LEDC_OVF_CNT_EN_CHn` is set to 1.
- `LEDC_DUTY_CHNG_END_CHn_INT`: Triggered when a fade on an LED PWM generator has finished.
- `LEDC_TIMERx_OVF_INT`: Triggered when an LED PWM timer has reached its maximum counter value.
```