

```markdown
Register 36.36. MCPWM_GEN1_B_REG (0x008C)

| 31 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | Reset |

MCPWM_GEN1_B_UTEZ Configures the action on PWM1B triggered by event TEZ when timer increasing.
O: No change
1: Low
2: High
3: Toggle
(R/W)

MCPWM_GEN1_B_UTEP Configures action on PWM1B triggered by event TEP when timer increasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_UTEA Configures action on PWM1B triggered by event TEA when timer increasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_UTEB Configures action on PWM1B triggered by event TEB when timer increasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_UT0 Configures action on PWM1B triggered by event_t0 when timer increasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_UT1 Configures action on PWM1B triggered by event_t1 when timer increasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_DTEZ Configures action on PWM1B triggered by event TEZ when timer decreasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_DTEP Configures action on PWM1B triggered by event TEP when timer decreasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_DTEA Configures action on PWM1B triggered by event TEA when timer decreasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_DTEB Configures action on PWM1B triggered by event TEB when timer decreasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_DTO Configures action on PWM1B triggered by event_t0 when timer decreasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)

MCPWM_GEN1_B_DT1 Configures action on PWM1B triggered by event_t1 when timer decreasing. See details in MCPWM_GEN1_B_UTEZ. (R/W)
```