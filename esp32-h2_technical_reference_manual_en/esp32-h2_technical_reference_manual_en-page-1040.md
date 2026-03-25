
```markdown
Chapter 35 LED PWM Controller (LEDC)

GoBack

35.3.6 Interrupts

*   LEDC_OVF_CNT_CHn_INT: Triggered when the timer counter overflows for `LEDC_OVF_NUM_CHn` + 1 times and the register `LEDC_OVF_CNT_EN_CHn` is set to 1. To trigger this interrupt, the field `LEDC_OVF_CNT_CHn_INT_ENA` of register `LEDC_INT_ENA_REG` should be set.
*   LEDC_DUTY_CHNG_END_CHn_INT: Triggered when a fade on an LED PWM generator has finished. To trigger this interrupt, the field `LEDC_DUTY_CHNG_END_CHn_INT_ENA` of register `LEDC_INT_ENA_REG` should be set.
*   LEDC_TIMERx_OVF_INT: Triggered when an LED PWM timer has reached its maximum counter value. To trigger this interrupt, the field `LEDC_TIMERx_OVF_INT_ENA` of register `LEDC_INT_ENA_REG` should be set.

Espressif Systems

1040
ESP32-H2 TRM (Version 1.1)

Submit Documentation Feedback
```