

```markdown
Register 36.35. MCPWM_GEN1_A_REG (0x0088)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | MCPWM_GEN1_A_DT1 | MCPWM_GEN1_A_DTO | MCPWM_GEN1_A_DTEB | MCPWM_GEN1_A_DTEA | MCPWM_GEN1_A_DTEP | MCPWM_GEN1_A_UTEZ | MCPWM_GEN1_A_UT0 | MCPWM_GEN1_A_UT1 | MCPWM_GEN1_A_UTEA | MCPWM_GEN1_A_UTEB | MCPWM_GEN1_A_UTE0 | MCPWM_GEN1_A_UTE1 | MCPWM_GEN1_A_UTE2 | MCPWM_GEN1_A_UTE3 | Reset |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

MCPWM_GEN1_A_UTEZ Configures action on PWM1A triggered by event TEZ when timer increasing.
O: No change
1: Low
2: High
3: Toggle
(R/W)

MCPWM_GEN1_A_UTE0 Configures action on PWM1A triggered by event TEP when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UTEA Configures action on PWM1A triggered by event TEA when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UTEB Configures action on PWM1A triggered by event TEB when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UT0 Configures action on PWM1A triggered by event_t0 when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UT1 Configures action on PWM1A triggered by event_t1 when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEZ Configures action on PWM1A triggered by event TEZ when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEP Configures action on PWM1A triggered by event TEP when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEA Configures action on PWM1A triggered by event TEA when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEB Configures action on PWM1A triggered by event TEB when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTO Configures action on PWM1A triggered by event_t0 when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DT1 Configures action on PWM1A triggered by event_t1 when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)
```