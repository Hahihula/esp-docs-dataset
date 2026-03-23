

```markdown
Register 36.27. MCPWM_FHO_CFGO_REG (0x0068)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

MCPWM_FHO_SW_CBC Configures whether or not to enable software force cycle-by-cycle mode action.
0: Disable
1: Enable
(R/W)

MCPWM_FHO_F2_CBC Configures whether or not fault_event2 will trigger cycle-by-cycle mode action.
0: Disable
1: Enable
(R/W)

MCPWM_FHO_F1_CBC Configures whether or not fault_event1 will trigger cycle-by-cycle mode action. See details in MCPWM_FHO_F2_CBC. (R/W)

MCPWM_FHO_FO_CBC Configures whether or not fault_eventO will trigger cycle-by-cycle mode action. See details in MCPWM_FHO_F2_CBC. (R/W)

MCPWM_FHO_SW_OST Configures whether or not to enable software force one-shot mode action.
See details in MCPWM_FHO_SW_CBC. (R/W)

MCPWM_FHO_F2_OST Configures whether or not fault_event2 will trigger one-shot mode action.
See details in MCPWM_FHO_F2_CBC. (R/W)

MCPWM_FHO_F1_OST Configures whether or not fault_event1 will trigger one-shot mode action.
See details in MCPWM_FHO_F2_CBC. (R/W)

MCPWM_FHO_FO_OST Configures whether or not fault_eventO will trigger one-shot mode action.
See details in MCPWM_FHO_F2_CBC. (R/W)

MCPWM_FHO_A_CBC_D Configures cycle-by-cycle mode action on PWM0A when fault event occurs and timer is decreasing.
0: Do nothing
1: Force low
2: Force high
3: Toggle
(R/W)

MCPWM_FHO_A_CBC_U Configures cycle-by-cycle mode action on PWM0A when fault event occurs and timer is increasing. See details in MCPWM_FHO_A_CBC_D. (R/W)
```