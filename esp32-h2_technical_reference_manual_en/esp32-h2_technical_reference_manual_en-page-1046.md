

```markdown
Register 35.3. LEDC_EVT_TASK_ENO_REG (0x01A0)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                             |                                                                             |
| 30  | LEDC_EVT_DUTY_CHNG_END_CHn_EN        | Configures whether or not to enable the LEDC_EVT_DUTY_CHNG_END_CHn event.   |
|     | O: Disable                           |                                                                                 |
|     | 1: Enable                            | (R/W)                                                                         |
| 29  | LEDC_EVT_OVF_CNT_PLS_CHn_EN           | Configures whether or not to enable the LEDC_EVT_OVF_CNT_PLS_CHn event.      |
|     | O: Disable                           |                                                                                 |
|     | 1: Enable                            | (R/W)                                                                         |
| 28  | LEDC_EVT_TIME_OVF_TIMERx_EN           | Configures whether or not to enable the LEDC_EVT_TIME_OVF_TIMERx event event.|
|     | O: Disable                           |                                                                                 |
|     | 1: Enable                            | (R/W)                                                                         |
| 27  | LEDC_EVT_TIME_CMP_EN                 | Configures whether or not to enable the LEDC_EVT_TIME_CMP event.            |
|     | O: Disable                           |                                                                                 |
|     | 1: Enable                            | (R/W)                                                                         |
| 26  | LEDC_TASK_DUTY_SCALE_UPDATE_CHn_EN    | Configures whether or not to enable the LEDC_TASK_DUTY_SCALE_UPDATE_CHn task.|
|     | O: Disable                           |                                                                                 |
|     | 1: Enable                            | (R/W)                                                                         |
```