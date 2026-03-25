
```markdown
value configured in the LEDC_TIMERx_DUTY_RES field at the next overflow of the counter.

*   `LEDC_TASK_TIMERx_CAP`: If the `LEDC_TASK_TIMERx_CAP_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_CAP` task, Timerx captures its counter’s value, and stores the value into the `LEDC_TIMERx_CNT_CAP` field of register `LEDC_TIMERx_CNT_CAP_REG`.

*   `LEDC_TASK_SIG_OUT_DIS_CHn`: If the `LEDC_TASK_SIG_OUT_DIS_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_SIG_OUT_DIS_CHn` task, PWMn’s signal output is disabled, and the output signal (`sig_out`) outputs a constant level as specified by field `IDC_IDE_LV_CHn`, as shown in Figure 35.3-1.

*   `LEDC_TASK_OVF_CNT_RST_CHn`: If the `LEDC_TASK_OVF_CNT_RST_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_OVF_CNT_RST_CHn` task, PWMn timer’s overflow counter is reset to 0.

*   `LEDC_TASK_TIMERx_RST`: If the `LEDC_TASK_TIMERx_RST_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_RST` task, Timerx’s counter is reset to 0.

*   `LEDC_TASK_TIMERx_PAUSE` and `LEDC_TASK_TIMERx_PAUSE`: If the `LEDC_TASK_TIMERx_PAUSE_RESUME_EN` field is enabled, upon receiving the `LEDC_TASK_TIMERx_PAUSE` and `LEDC_TASK_TIMERx_PAUSE` task, Timerx is suspended and resumed alternately. That is, when the task is received, Timerx is paused; and when the task is received again, Timerx is resumed.

*   `LEDC_TASK_GAMMA_RESTART_CHn`: If the `LEDC_TASK_GAMMA_RESTART_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_GAMMA_RESTART_CHn` task, the PWMn restarts to generate the fading PWM signal.

*   `LEDC_TASK_GAMMA_PAUSE_CHn`: If the `LEDC_TASK_GAMMA_PAUSE_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_GAMMA_PAUSE_CHn` task, PWMn suspends Duty Cycle Fading at the next timer overflow. That is, after the task has been received, PWMn keeps the duty cycle of the last fade.

*   `LEDC_TASK_GAMMA_RESUME_CHn`: If the `LEDC_TASK_GAMMA_RESUME_CHn_EN` field is enabled, upon receiving the `LEDC_TASK_GAMMA_RESUME_CHn` task, PWMn resumes Duty Cycle Fading at the next counter overflow. That is, after the task has been received, PWMn resumes fading from the range where the suspension occurs.

LEDC can generate the following ETM events:

*   `LEDC_EVT_DUTY_CHNG_END_CHn`: Generated when the `LEDC_EVT_DUTY_CHNG_END_CHn_EN` field is enabled, and PWMn has finished Duty Cycle Fading.

*   `LEDC_EVT_OVF_CNT_PLS_CHn`: Generated when the `LEDC_EVT_OVF_CNT_PLS_CHn_EN` field is enabled and when PWMn timer’s counter overflows for `LEDC_OVF_NUM_CHn + 1` times.

*   `LEDC_EVT_TIME_OVF_TIMERx`: Generated when the `LEDC_EVT_TIME_OVF_TIMERx_EN` field is enabled and Timerx’s counter overflows.

*   `LEDC_EVT_TIMERx_CMP`: Generated when the `LEDC_EVT_TIMEx_CMP_EN` field is enabled and the value of Timerx’s counter reaches that of the `LEDC_TIMERx_CMP` field of register `LEDC_TIMERx_CMP_REG`.

In practical applications, LEDC’s ETM events can trigger its own ETM tasks. For example,
`LEDC_EVT_DUTY_CHNG_END_CHn` event can trigger the `LEDC_TASK_GAMMA_RESTART_CHn` task, thus starting the next fading directly after the current fading is completed.
```