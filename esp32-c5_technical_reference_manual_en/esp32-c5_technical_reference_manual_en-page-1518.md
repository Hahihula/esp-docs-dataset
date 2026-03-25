

```markdown
Register 40.8. LEDC_EVT_TASK_EN1_REG (0x0124)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

LEDC_TASK_TIMERx_RES_UPDATE_EN (x: 0-3) Configures whether to enable LEDC_TASK_TIMERx_RES_UPDATE task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_TIMERx_CAP_EN (x: 0-3) Configures whether to enable LEDC_TASK_TIMERx_CAP task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_SIG_OUT_DIS_CHn_EN (n: 0-5) Configures whether to enable LEDC_TASK_SIG_OUT_DIS_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_OVF_CNT_RST_CHn_EN (n: 0-5) Configures whether to enable LEDC_TASK_OVF_CNT_RST_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_TIMERx_RST_EN (x: 0-3) Configures whether to enable LEDC_TASK_TIMERx_RST task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_TIMERx_PAUSE_RESUME_EN (x: 0-3) Configures whether to enable LEDC_TASK_TIMERx_PAUSE and LEDC_TASK_TIMERx_RESUME task.
O: Disable
1: Enable
(R/W)
```