

```markdown
Register 35.3. LEDC_EVT_TASK_ENO_REG (0x01A0)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | LEDC_TASK_DUTY_SCALE_UPDATE_CH4_EN        | Configures whether or not to enable the LEDC_TASK_DUTY_SCALE_UPDATE_CH4_EN task. O: Disable<br>1: Enable<br>(R/W) |
| 29  | LEDC_TASK_DUTY_SCALE_UPDATE_CH3_EN        |                                                                             |
| 28  | LEDC_TASK_DUTY_SCALE_UPDATE_CH2_EN        |                                                                             |
| 27  | LEDC_TASK_DUTY_SCALE_UPDATE_CH1_EN        |                                                                             |
| 26  | LEDC_TASK_DUTY_SCALE_UPDATE_CH0_EN        |                                                                             |
| 25  | (reserved)                                |                                                                             |
| 24  | LEDC_EVT_OVF_CNT_PLS_CH4_EN               | Configures whether or not to enable the LEDC_EVT_OVF_CNT_PLS_CH4_EN event. O: Disable<br>1: Enable<br>(R/W) |
| 23  | LEDC_EVT_OVF_CNT_PLS_CH3_EN               |                                                                             |
| 22  | LEDC_EVT_OVF_CNT_PLS_CH2_EN               |                                                                             |
| 21  | LEDC_EVT_OVF_CNT_PLS_CH1_EN               |                                                                             |
| 20  | LEDC_EVT_OVF_CNT_PLS_CH0_EN               |                                                                             |
| 19  | (reserved)                                |                                                                             |
| 18  | LEDC_EVT_TIME_OVF_TIMER3_EN               | Configures whether or not to enable the LEDC_EVT_TIME_OVF_TIMER3 event. O: Disable<br>1: Enable<br>(R/W) |
| 17  | LEDC_EVT_TIME_OVF_TIMER2_EN               |                                                                             |
| 16  | LEDC_EVT_TIME_OVF_TIMER1_EN               |                                                                             |
| 15  | (reserved)                                |                                                                             |
| 14  | LEDC_EVT_TIME_CMP0_EN                     | Configures whether or not to enable the LEDC_EVT_TIME_CMP0 event. O: Disable<br>1: Enable<br>(R/W) |
| 13  | LEDC_EVT_TIME_CMP1_EN                     |                                                                             |
| 12  | LEDC_EVT_TIME_CMP2_EN                     |                                                                             |
| 11  | (reserved)                                |                                                                             |
| 10  | LEDC_EVT_DUTY_CHNG_END_CH4_EN             | Configures whether or not to enable the LEDC_EVT_DUTY_CHNG_END_CH4 event. O: Disable<br>1: Enable<br>(R/W) |
| 9   | LEDC_EVT_DUTY_CHNG_END_CH3_EN             |                                                                             |
| 8   | LEDC_EVT_DUTY_CHNG_END_CH2_EN             |                                                                             |
| 7   | LEDC_EVT_DUTY_CHNG_END_CH1_EN             |                                                                             |
| 6   | LEDC_EVT_DUTY_CHNG_END_CH0_EN             |                                                                             |
| 5   | (reserved)                                |                                                                             |
| 4   | Reset                                     |                                                                             |
| 3   | O                                        |                                                                             |
| 2   | 1                                        |                                                                             |
| 1   | 0                                        |                                                                             |
| 0   | Reset                                     |                                                                             |

LEDC_EVT_DUTY_CHNG_END_CHn_EN (n: 0-5) Configures whether or not to enable the LEDC_EVT_DUTY_CHNG_END_CHn event.
O: Disable
1: Enable
(R/W)

LEDC_EVT_OVF_CNT_PLS_CHn_EN (n: 0-5) Configures whether or not to enable the LEDC_EVT_OVF_CNT_PLS_CHn event.
O: Disable
1: Enable
(R/W)

LEDC_EVT_TIME_OVF_TIMERx_EN (x: 0-3) Configures whether or not to enable the LEDC_EVT_TIME_OVF_TIMERx event event.
O: Disable
1: Enable
(R/W)

LEDC_EVT_TIMEx_CMP_EN (x: 0-3) Configures whether or not to enable the LEDC_EVT_TIMERx_CMP event.
O: Disable
1: Enable
(R/W)

LEDC_TASK_DUTY_SCALE_UPDATE_CHn_EN (n: 0-5) Configures whether or not to enable the LEDC_TASK_DUTY_SCALE_UPDATE_CHn task.
O: Disable
1: Enable
(R/W)
```