

```markdown
Register 36.50. MCPWM_GEN2_B_REG (0x0004)

| 31 | (reserved) | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|------------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0   | 0          | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

MCPWM_GEN2_B_UTEZ    Action on PWM2B triggered by event TEZ when timer increasing.
O: No change
1: Low
2: High
3: Toggle
(R/W)

MCPWM_GEN2_B_UTEP    Action on PWM2B triggered by event TEP when timer increasing. (R/W)
MCPWM_GEN2_B_UTEA    Action on PWM2B triggered by event TEA when timer increasing. (R/W)
MCPWM_GEN2_B_UTEB    Action on PWM2B triggered by event TEB when timer increasing. (R/W)
MCPWM_GEN2_B_UT0     Action on PWM2B triggered by event_t0 when timer increasing. (R/W)
MCPWM_GEN2_B_UT1     Action on PWM2B triggered by event_t1 when timer increasing. (R/W)
MCPWM_GEN2_B_DTEZ    Action on PWM2B triggered by event TEZ when timer decreasing. (R/W)
MCPWM_GEN2_B_DTEP    Action on PWM2B triggered by event TEP when timer decreasing. (R/W)
MCPWM_GEN2_B_DTEA    Action on PWM2B triggered by event TEA when timer decreasing. (R/W)
MCPWM_GEN2_B_DTEB    Action on PWM2B triggered by event TEB when timer decreasing. (R/W)
MCPWM_GEN2_B_DTO     Action on PWM2B triggered by event_t0 when timer decreasing. (R/W)
MCPWM_GEN2_B_DT1     Action on PWM2B triggered by event_t1 when timer decreasing. (R/W)
```