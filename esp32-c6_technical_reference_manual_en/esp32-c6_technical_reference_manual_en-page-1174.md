

```markdown
next counter overflow. That is, after the task has been received, PWMn resumes fading from the range where the suspension occurs.

LEDC can generate the following ETM events:

*   LEDC_EVT_DUTY_CHNG_END_CHn: Generated when the LEDC_EVT_DUTY_CHNG_END_CHn_EN field is enabled, and PWMn has finished Duty Cycle Fading.
*   LEDC_EVT_OVF_CNT_PLS_CHn: Generated when the LEDC_EVT_OVF_CNT_PLS_CHn_EN field is enabled and when PWMn timer’s counter overflows for LEDC_OVF_NUM_CHn + 1 times.
*   LEDC_EVT_TIME_OVF_TIMERx: Generated when the LEDC_EVT_TIME_OVF_TIMERx_EN field is enabled and Timerx’s counter overflows.
*   LEDC_EVT_TIMERx_CMP: Generated when the LEDC_EVT_TIMEx_CMP_EN field is enabled and the value of Timerx’s counter reaches that of the LEDC_TIMERx_CMP field of register LEDC_TIMERx_CMP_REG.

In practical applications, LEDC’s ETM events can trigger its own ETM tasks. For example, LEDC_EVT_DUTY_CHNG_END_CHn event can trigger the LEDC_TASK_GAMMA_RESTART_CHn task, thus starting the next fading directly after the current fading is completed.

### 35.3.6 Interrupts

*   LEDC_OVF_CNT_CHn_INT: Triggered when the timer counter overflows for LEDC_OVF_NUM_CHn + 1 times and the register LEDC_OVF_CNT_EN_CHn is set to 1. To trigger this interrupt, the field LEDC_OVF_CNT_CHn_INT_ENA of register LEDC_INT_ENA_REG should be set.
*   LEDC_DUTY_CHNG_END_CHn_INT: Triggered when a fade on an LED PWM generator has finished. To trigger this interrupt, the field LEDC_DUTY_CHNG_END_CHn_INT_ENA of register LEDC_INT_ENA_REG should be set.
*   LEDC_TIMERx_OVF_INT: Triggered when an LED PWM timer has reached its maximum counter value. To trigger this interrupt, the field LEDC_TIMERx_OVF_INT_ENA of register LEDC_INT_ENA_REG should be set.
```