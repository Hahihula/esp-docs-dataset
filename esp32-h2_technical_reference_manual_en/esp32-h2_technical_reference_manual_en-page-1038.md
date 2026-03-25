

```markdown
Chapter 35 LED PWM Controller (LEDC)
GoBack

Figure 35.3-6. Output Signal of Gamma Curve Fading

35.3.4.3 Suspend and Resume Duty Cycle Fading

To suspend Duty Cycle Fading that has already been started, write 1 to the `LEDC_CHn_GAMMA_PAUSE` field of the `LEDC_CHn_GAMMA_CONF_REG` register. Once `LEDC_CHn_GAMMA_PAUSE` is set to 1, the PWM signal keeps the duty cycle of the most recent fade.

To resume Duty Cycle Fading, write 1 to the `LEDC_CHn_GAMMA_RESUME` field of the `LEDC_CHn_GAMMA_CONF_REG` register. Once `LEDC_CHn_GAMMA_RESUME` is set to 1, the PWM signal resumes fading from the range where the suspension occurs, until fading in the last range finishes. The fading will continue from the state when it was paused until all the ranges complete duty cycle fading (when `LEDC_CHn_GAMMA_RESUME` is set to 1, `LEDC_CHn_GAMMA_PAUSE` is cleared automatically by hardware).

35.3.5 Event Task Matrix Feature

The LEDC on ESP32-H2 supports the Event Task Matrix (ETM) function, which allows LEDC’s ETM tasks to be triggered by any peripherals’ ETM events, or LEDC’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to LEDC. For more information, please refer to Chapter 10 Event Task Matrix (SOC_ETM).

ETM-related events and tasks are enabled by configuring corresponding fields of `LEDC_EVT_TASK_ENO_REG`, `LEDC_EVT_TASK_EN1_REG` and `LEDC_EVT_TASK_EN2_REG` registers. For the correspondence between events, tasks, and fields, Please refer to Section 35.5).

LEDC can receive the following ETM tasks:

*   `LEDC_TASK_DUTY_SCALE_UPDATE_CHn`: If the `LEDC_TASK_DUTY_SCALE_UPDATE_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_DUTY_SCALE_UPDATE_CHn` task, PWMn generates fading PWM signals according to the newly configured `LEDC_CHn_GAMMA_SCALE` field.
*   `LEDC_TASK_TIMERx_RES_UPDATE`: If the `LEDC_TASK_TIMERx_RES_UPDATE_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_RES_UPDATE` task, Timerx updates its counter’s overflow value to the
```