

```markdown
Register 36.35. MCPWM_GEN1_A_REG (0x0088)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | MCPWM_GEN1_A_DT1                     | Configures action on PWM1A triggered by event_t1 when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 29  | MCPWM_GEN1_A_DTO                     | Configures action on PWM1A triggered by event_t0 when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 28  | MCPWM_GEN1_A_DTEB                    | Configures action on PWM1A triggered by event TEB when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 27  | MCPWM_GEN1_A_DTEA                    | Configures action on PWM1A triggered by event TEA when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 26  | MCPWM_GEN1_A_DTEP                    | Configures action on PWM1A triggered by event TEP when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 25  | MCPWM_GEN1_A_UT0                     | Configures action on PWM1A triggered by event_t0 when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 24  | MCPWM_GEN1_A_UT1                     | Configures action on PWM1A triggered by event_t1 when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 23  | MCPWM_GEN1_A_UTEZ                    | Configures action on PWM1A triggered by event TEZ when timer increasing.<br>0: No change<br>1: Low<br>2: High<br>3: Toggle (R/W) |
| 22  | MCPWM_GEN1_A_UTEA                    | Configures action on PWM1A triggered by event TEA when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 21  | MCPWM_GEN1_A_UTEB                    | Configures action on PWM1A triggered by event TEB when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |
| 20  | MCPWM_GEN1_A_UTEP                    | Configures action on PWM1A triggered by event TEP when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W) |

MCPWM_GEN1_A_UTEZ   Configures action on PWM1A triggered by event TEZ when timer increasing.
0: No change
1: Low
2: High
3: Toggle
(R/W)

MCPWM_GEN1_A_UTEZ   See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UTEA   Configures action on PWM1A triggered by event TEA when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UTEB   Configures action on PWM1A triggered by event TEB when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UT0    Configures action on PWM1A triggered by event_t0 when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_UT1    Configures action on PWM1A triggered by event_t1 when timer increasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEZ   Configures action on PWM1A triggered by event TEZ when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEP   Configures action on PWM1A triggered by event TEP when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEA   Configures action on PWM1A triggered by event TEA when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTEB   Configures action on PWM1A triggered by event TEB when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DTO    Configures action on PWM1A triggered by event_t0 when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)

MCPWM_GEN1_A_DT1    Configures action on PWM1A triggered by event_t1 when timer decreasing. See details in MCPWM_GEN1_A_UTEZ. (R/W)
```