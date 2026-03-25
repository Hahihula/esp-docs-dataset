

```markdown
Register 35.4. LEDC_EVT_TASK_EN1_REG (0x0A4)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                            |                                                                             |
| 30  | LEDC_TASK_TIMER3_PAUSE_RESUME_EN    | Configures whether or not to enable the LEDC_TASK_TIMER3_PAUSE_RESUME task. O: Disable<br>1: Enable (R/W) |
| 29  | LEDC_TASK_TIMER2_PAUSE_RESUME_EN    | Configures whether or not to enable the LEDC_TASK_TIMER2_PAUSE_RESUME task. O: Disable<br>1: Enable (R/W) |
| 28  | LEDC_TASK_TIMER1_PAUSE_RESUME_EN    | Configures whether or not to enable the LEDC_TASK_TIMER1_PAUSE_RESUME task. O: Disable<br>1: Enable (R/W) |
| 27  | LEDC_TASK_TIMER0_PAUSE_RESUME_EN    | Configures whether or not to enable the LEDC_TASK_TIMER0_PAUSE_RESUME task. O: Disable<br>1: Enable (R/W) |
| 26  | LEDC_TASK_OVF_CNT_RST_RST_EN        | Configures whether or not to enable the LEDC_TASK_OVF_CNT_RST_CHn task. O: Disable<br>1: Enable (R/W) |
| 25  | LEDC_TASK_SIG_OUT_DIS_CH4_EN        | Configures whether or not to enable the LEDC_TASK_SIG_OUT_DIS_CH4 task. O: Disable<br>1: Enable (R/W) |
| 24  | LEDC_TASK_SIG_OUT_DIS_CH3_EN        | Configures whether or not to enable the LEDC_TASK_SIG_OUT_DIS_CH3 task. O: Disable<br>1: Enable (R/W) |
| 23  | LEDC_TASK_SIG_OUT_DIS_CH2_EN        | Configures whether or not to enable the LEDC_TASK_SIG_OUT_DIS_CH2 task. O: Disable<br>1: Enable (R/W) |
| 22  | LEDC_TASK_SIG_OUT_DIS_CH1_EN        | Configures whether or not to enable the LEDC_TASK_SIG_OUT_DIS_CH1 task. O: Disable<br>1: Enable (R/W) |
| 21  | LEDC_TASK_OVF_CNT_RST_CH4_EN        | Configures whether or not to enable the LEDC_TASK_OVF_CNT_RST_CH4 task. O: Disable<br>1: Enable (R/W) |
| 20  | LEDC_TASK_OVF_CNT_RST_CH3_EN        | Configures whether or not to enable the LEDC_TASK_OVF_CNT_RST_CH3 task. O: Disable<br>1: Enable (R/W) |
| 19  | LEDC_TASK_OVF_CNT_RST_CH2_EN        | Configures whether or not to enable the LEDC_TASK_OVF_CNT_RST_CH2 task. O: Disable<br>1: Enable (R/W) |
| 18  | LEDC_TASK_OVF_CNT_RST_CH1_EN        | Configures whether or not to enable the LEDC_TASK_OVF_CNT_RST_CH1 task. O: Disable<br>1: Enable (R/W) |
| 17  | Reserved                            |                                                                             |
| 16  | LEDC_TASK_SIG_OUT_DIS_CH0_EN        | Configures whether or not to enable the LEDC_TASK_SIG_OUT_DIS_CH0 task. O: Disable<br>1: Enable (R/W) |
| 15  | LEDC_TASK_TIMER3_CAP_EN             | Configures whether or not to enable the LEDC_TASK_TIMER3_CAP task. O: Disable<br>1: Enable (R/W) |
| 14  | LEDC_TASK_TIMER2_CAP_EN             | Configures whether or not to enable the LEDC_TASK_TIMER2_CAP task. O: Disable<br>1: Enable (R/W) |
| 13  | LEDC_TASK_TIMER1_CAP_EN             | Configures whether or not to enable the LEDC_TASK_TIMER1_CAP task. O: Disable<br>1: Enable (R/W) |
| 12  | LEDC_TASK_TIMER0_CAP_EN             | Configures whether or not to enable the LEDC_TASK_TIMER0_CAP task. O: Disable<br>1: Enable (R/W) |
| 11  | Reserved                            |                                                                             |
| 10  | LEDC_TASK_RES_UPDATE_EN             | Configures whether or not to enable the LEDC_TASK_RES_UPDATE task. O: Disable<br>1: Enable (R/W) |
| 9   | LEDC_TASK_TIMER3_RES_UPDATE_task    |                                                                             |
| 8   | LEDC_TASK_TIMER2_RES_UPDATE_task    |                                                                             |
| 7   | LEDC_TASK_TIMER1_RES_UPDATE_task    |                                                                             |
| 6   | LEDC_TASK_TIMER0_RES_UPDATE_task    |                                                                             |
| 5   | Reserved                            |                                                                             |
| 4   | LEDC_TASK_SIG_OUT_DIS_CHn_EN        | Configures whether or not to enable the LEDC_TASK_SIG_OUT_DIS_CHn task. O: Disable<br>1: Enable (R/W) |
| 3   | LEDC_TASK_OVF_CNT_RST_CHn_EN        | Configures whether or not to enable the LEDC_TASK_OVF_CNT_RST_CHn task. O: Disable<br>1: Enable (R/W) |
| 2   | Reserved                            |                                                                             |
| 1   | Reset                                |                                                                             |
| 0   | Reset                                |                                                                             |

LEDC_TASK_TIMERx_RES_UPDATE_EN Configures whether or not to enable the LEDC_TASK_TIMERx_RES_UPDATE task.
O: Disable
1: Enable (R/W)

LEDC_TASK_TIMERx_CAP_EN Configures whether or not to enable the LEDC_TASK_TIMERx_CAP task.
O: Disable
1: Enable (R/W)

LEDC_TASK_SIG_OUT_DIS_CHn_EN Configures whether or not to enable the LEDC_TASK_SIG_OUT_DIS_CHn task.
O: Disable
1: Enable (R/W)

LEDC_TASK_OVF_CNT_RST_CHn_EN Configures whether or not to enable the LEDC_TASK_OVF_CNT_RST_CHn task.
O: Disable
1: Enable (R/W)

LEDC_TASK_TIMERx_RST_EN Configures whether or not to enable the LEDC_TASK_TIMERx_RST task.
O: Disable
1: Enable (R/W)

LEDC_TASK_TIMERx_PAUSE_RESUME_EN Configures whether or not to enable the LEDC_TASK_TIMERx_RESUME and LEDC_TASK_TIMERx_PAUSE task.
O: Disable
1: Enable (R/W)
```