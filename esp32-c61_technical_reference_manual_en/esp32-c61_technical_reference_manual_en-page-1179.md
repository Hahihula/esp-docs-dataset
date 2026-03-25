

```markdown
Chapter 31 LED PWM Controller (LEDC) GoBack


Register 31.9. LEDC_EVT_TASK_EN2_REG (0x0128)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 24  | LEDC_TASK_GAMMA_RESTART_CH5_EN            | Configures whether to enable LEDC_TASK_GAMMA_RESTART_CH5 task.              |
| 20  | LEDC_TASK_GAMMA_RESTART_CH4_EN            | Configures whether to enable LEDC_TASK_GAMMA_RESTART_CH4 task.              |
| 19  | LEDC_TASK_GAMMA_RESTART_CH3_EN            | Configures whether to enable LEDC_TASK_GAMMA_RESTART_CH3 task.              |
| 18  | LEDC_TASK_GAMMA_RESTART_CH2_EN            | Configures whether to enable LEDC_TASK_GAMMA_RESTART_CH2 task.              |
| 17  | LEDC_TASK_GAMMA_RESTART_CH1_EN            | Configures whether to enable LEDC_TASK_GAMMA_RESTART_CH1 task.              |
| 16  | LEDC_TASK_GAMMA_RESTART_CH0_EN            | Configures whether to enable LEDC_TASK_GAMMA_RESTART_CH0 task.              |
| 15  | LEDC_TASK_GAMMA_PAUSE_CH5_EN              | Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CH5 task.                |
| 14  | LEDC_TASK_GAMMA_PAUSE_CH4_EN              | Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CH4 task.                |
| 13  | LEDC_TASK_GAMMA_PAUSE_CH3_EN              | Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CH3 task.                |
| 12  | LEDC_TASK_GAMMA_PAUSE_CH2_EN              | Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CH2 task.                |
| 11  | LEDC_TASK_GAMMA_PAUSE_CH1_EN              | Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CH1 task.                |
| 10  | LEDC_TASK_GAMMA_PAUSE_CH0_EN              | Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CH0 task.                |
| 9   | LEDC_TASK_GAMMA_RESUME_CH5_EN             | Configures whether to enable LEDC_TASK_GAMMA_RESUME_CH5 task.               |
| 8   | LEDC_TASK_GAMMA_RESUME_CH4_EN             | Configures whether to enable LEDC_TASK_GAMMA_RESUME_CH4 task.               |
| 7   | LEDC_TASK_GAMMA_RESUME_CH3_EN             | Configures whether to enable LEDC_TASK_GAMMA_RESUME_CH3 task.               |
| 6   | LEDC_TASK_GAMMA_RESUME_CH2_EN             | Configures whether to enable LEDC_TASK_GAMMA_RESUME_CH2 task.               |
| 5   | LEDC_TASK_GAMMA_RESUME_CH1_EN             | Configures whether to enable LEDC_TASK_GAMMA_RESUME_CH1 task.               |
| 4   | LEDC_TASK_GAMMA_RESUME_CH0_EN             | Configures whether to enable LEDC_TASK_GAMMA_RESUME_CH0 task.               |
| 3-0 | (reserved)                                |                                                                             |

LEDC_TASK_GAMMA_RESTART_CHn_EN (n: 0-5)   Configures whether to enable LEDC_TASK_GAMMA_RESTART_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_GAMMA_PAUSE_CHn_EN (n: 0-5)      Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_GAMMA_RESUME_CHn_EN (n: 0-5)     Configures whether to enable LEDC_TASK_GAMMA_RESUME_CHn task.
O: Disable
1: Enable
(R/W)


Register 31.10. LEDC_TIMERx_CMP_REG (x: 0-3) (0x0140+0x4*x)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 20  | LEDC_TIMERx_CMP                           | Configures the comparison value for LEDC timer x. (R/W)                     |
| 19  | (reserved)                                |                                                                             |
| 0   | Reset                                     |                                                                             |

LEDC_TIMERx_CMP    Configures the comparison value for LEDC timer x. (R/W)
```