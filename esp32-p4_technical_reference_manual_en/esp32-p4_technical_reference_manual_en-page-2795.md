
```markdown
Register 55.9. LEDC_EVT_TASK_EN2_REG (0x0128)

| Bit | Name                                      | Description                                                                 |
|-----|-------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                               |                                                                             |
| 30-24| LEDC_TASK_GAMMA_RESTART_CHn_EN           | Configures whether to enable LEDC_TASK_GAMMA_RESTART_CHn task.              |
|     | O: Disable                               |                                                                                 |
|     | 1: Enable                                | (R/W)                                                                         |
| 23-17| LEDC_TASK_GAMMA_PAUSE_CHn_EN             | Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CHn task.                |
|     | O: Disable                               |                                                                                 |
|     | 1: Enable                                | (R/W)                                                                         |
| 16-10| LEDC_TASK_GAMMA_RESUME_CHn_EN            | Configures whether to enable LEDC_TASK_GAMMA_RESUME_CHn task.               |
|     | O: Disable                               |                                                                                 |
|     | 1: Enable                                | (R/W)                                                                         |

Register 55.10. LEDC_TIMERx_CMP_REG (x: 0-3) (0x0140+0x4*x)

| Bit | Name                                      | Description                                                                 |
|-----|-------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                               |                                                                             |
| 20-0 | LEDC_TIMERx_CMP                          | Configures the comparison value for LEDC timer x.                           |
|     | O: 0x000                                  | (R/W)                                                                         |

```
```plaintext
LEDC_TASK_GAMMA_RESTART_CHn_EN (n: 0-7)   Configures whether to enable LEDC_TASK_GAMMA_RESTART_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_GAMMA_PAUSE_CHn_EN (n: 0-7)     Configures whether to enable LEDC_TASK_GAMMA_PAUSE_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TASK_GAMMA_RESUME_CHn_EN (n: 0-7)    Configures whether to enable LEDC_TASK_GAMMA_RESUME_CHn task.
O: Disable
1: Enable
(R/W)

LEDC_TIMERx_CMP                          Configures the comparison value for LEDC timer x. (R/W)
```