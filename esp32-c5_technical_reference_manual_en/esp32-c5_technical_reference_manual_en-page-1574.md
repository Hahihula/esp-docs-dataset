

```markdown
Register 41.13. MCPWM_GENn_A_REG(n: 0-2) (0x0050+0x38*n)

| 31 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | Reset |

MCPWM_GENn_A_UTEZ Configures action on PWMn A triggered by event TEZ when timer increasing.
O: No change
1: Low
2: High
3: Toggle
(R/W)

MCPWM_GENn_A_UTEP Configures action on PWMn A triggered by event TEP when timer increasing.
O: No change
1: Low
2: High
3: Toggle
(R/W)

MCPWM_GENn_A_UTEA Configures action on PWMn A triggered by event TEA when timer increasing.
O: No change
1: Low
2: High
3: Toggle
(R/W)

MCPWM_GENn_A_UTEB Configures action on PWMn A triggered by event TEB when timer increasing.
O: No change
1: Low
2: High
3: Toggle
(R/W)
```
Continued on the next page...
```