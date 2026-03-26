
```markdown
LEDC_CHn_GAMMA_RESUME is set to 1, LEDC_CHn_GAMMA_PAUSE is cleared automatically by hardware.

55.4.4 Event Task Matrix Feature

The LEDC on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows LEDC’s ETM tasks to be triggered by any peripherals’ ETM events, or LEDC’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to LEDC. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

ETM-related events and tasks are enabled by configuring corresponding fields of `LEDC_EVT_TASK_EN0_REG`, `LEDC_EVT_TASK_EN1_REG` and `LEDC_EVT_TASK_EN2_REG` registers. For the correspondence between events, tasks, and fields, Please refer to Section 55.8).

LEDC can receive the following ETM tasks:

*   `LEDC_TASK_DUTY_SCALE_UPDATE_CHn`: If the `LEDC_TASK_DUTY_SCALE_UPDATE_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_DUTY_SCALE_UPDATE_CHn` task, PWMn generates fading PWM signals according to the newly configured `LEDC_CHn_GAMMA_SCALE` field.
*   `LEDC_TASK_TIMERx_RES_UPDATE`: If the `LEDC_TASK_TIMERx_RES_UPDATE_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_RES_UPDATE` task, Timerx updates its counter’s overflow value to the value configured in the `LEDC_TIMERx_DUTY_RES` field at the next overflow of the counter.
*   `LEDC_TASK_TIMERx_CAP`: If the `LEDC_TASK_TIMERx_CAP_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_CAP` task, Timerx captures its counter’s value, and stores the value into the `LEDC_TIMERx_CNT_CAP` field of register `LEDC_TIMERx_CNT_CAP_REG`.
*   `LEDC_TASK_SIG_OUT_DIS_CHn`: If the `LEDC_TASK_SIG_OUT_DIS_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_SIG_OUT_DIS_CHn` task, PWMn’s signal output is disabled, and the output signal (`sig_outn`) outputs a constant level as specified by field `LEDC_IDLE_LV_CHn`, as shown in Figure 55.3-2.
*   `LEDC_TASK_OVF_CNT_RST_CHn`: If the `LEDC_TASK_OVF_CNT_RST_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_OVF_CNT_RST_CHn` task, PWMn timer’s overflow counter is reset to 0.
*   `LEDC_TASK_TIMERx_RST`: If the `LEDC_TASK_TIMERx_RST_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_RST` task, Timerx’s counter is reset to 0.
*   `LEDC_TASK_TIMERx_RESULT` and `LEDC_TASK_TIMERx_PAUSE`: If the `LEDC_TASK_TIMERx_PAUSE_RESUME_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_PAUSE` task, Timerx is suspended and resumed alternately. That is, when the task is received, Timerx is paused; and when the task is received again, Timerx is resumed.
*   `LEDC_TASK_GAMMA_RESTART_CHn`: If the `LEDC_TASK_GAMMA_RESTART_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_GAMMA_RESTART_CHn` task, PWMn restarts to generate the fading PWM signal.
*   `LEDC_TASK_GAMMA_PAUSE_CHn`: If the `LEDC_TASK_GAMMA_PAUSE_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_GAMMA_PAUSE_CHn` task, PWMn suspends Duty Cycle Fading at the next timer overflow. That is, after the task has been received, PWMn keeps the duty cycle of the last fade.
```