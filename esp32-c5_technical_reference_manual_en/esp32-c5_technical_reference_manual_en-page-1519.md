
```markdown
Register 40.9. LEDC_EVT_TASK_EN2_REG (0x0128)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | LEDC_TASK_GAMMA_RESTART_CH5_EN | LEDC_TASK_GAMMA_RESTART_CH4_EN | LEDC_TASK_GAMMA_RESTART_CH3_EN | LEDC_TASK_GAMMA_RESTART_CH2_EN | LEDC_TASK_GAMMA_RESTART_CH1_EN | LEDC_TASK_GAMMA_RESTART_CH0_EN |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | LEDC_TASK_GAMMA_PAUSE_CH5_EN | LEDC_TASK_GAMMA_PAUSE_CH4_EN | LEDC_TASK_GAMMA_PAUSE_CH3_EN | LEDC_TASK_GAMMA_PAUSE_CH2_EN | LEDC_TASK_GAMMA_PAUSE_CH1_EN | LEDC_TASK_GAMMA_PAUSE_CH0_EN |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | LEDC_TASK_GAMMA_RESTART_CH5_EN | LEDC_TASK_GAMMA_RESTART_CH4_EN | LEDC_TASK_GAMMA_RESTART_CH3_EN | LEDC_TASK_GAMMA_RESTART_CH2_EN | LEDC_TASK_GAMMA_RESTART_CH1_EN | LEDC_TASK_GAMMA_RESTART_CH0_EN |

LEDC_TASK_GAMMA_RESTART_CHn_EN (n: 0-5) Configures whether to enable
LEDC_TASK_GAMMA_RESTART_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_GAMMA_PAUSE_CHn_EN (n: 0-5) Configures whether to enable
LEDC_TASK_GAMMA_PAUSE_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_GAMMA_RESUME_CHn_EN (n: 0-5) Configures whether to enable
LEDC_TASK_GAMMA_RESUME_CHn task.
O: Disable
1: Enable
(R/W)
```

Register 40.10. LEDC_TIMERx_CMP_REG (x: 0-3) (0x0140+0x4*x)

| Bit | 31 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | (reserved) |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | LEDC_TIMERx_CMP | 0x000 | Reset |

LEDC_TIMERx_CMP Configures the comparison value for LEDC timer x. (R/W)
```