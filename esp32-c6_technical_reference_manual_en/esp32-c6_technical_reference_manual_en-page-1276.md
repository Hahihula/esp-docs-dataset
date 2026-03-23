

```markdown
Register 36.55. MCPWM_FH2_CFG0_REG (0x00D8)

| 31 | (reserved) | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|-----------:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
|    |            | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

MCPWM_FH2_SW_CBC Configures whether or not to enable software force cycle-by-cycle mode action.
O: Disable
1: Enable
(R/W)

MCPWM_FH2_F2_CBC Configures whether or not fault_event2 will trigger cycle-by-cycle mode action.
O: No effect
1: Trigger
(R/W)

MCPWM_FH2_F1_CBC Configures whether or not fault_event1 will trigger cycle-by-cycle mode action.
O: No effect
1: Trigger
(R/W)

MCPWM_FH2_F0_CBC Configures whether or not fault_event0 will trigger cycle-by-cycle mode action.
O: No effect
1: Trigger
(R/W)

MCPWM_FH2_SW_OST Configures whether or not to enable software force one-shot mode action.
O: Disable
1: Enable
(R/W)

MCPWM_FH2_F2_OST Configures whether or not fault_event2 will trigger one-shot mode action.
O: No effect
1: Trigger
(R/W) (R/W)

MCPWM_FH2_F1_OST Configures whether or not fault_event1 will trigger one-shot mode action.
O: No effect
1: Trigger
(R/W) (R/W)
```
Continued on the next page...
```