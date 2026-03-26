

```markdown
Register 56.19. MCPWM_FHn_CFGO_REG(n: 0-2) (0x0068+0x38*n)

| 31 | (reserved) | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|------------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0   |            |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

MCPWM_TZn_SW_CBC Configures whether to enable software force cycle-by-cycle mode action.
O: Disable
1: Enable
(R/W)

MCPWM_TZn_F2_CBC Configures whether event_f2 will trigger cycle-by-cycle mode action.
O: Disable
1: Enable
(R/W)

MCPWM_TZn_F1_CBC Configures whether event_f1 will trigger cycle-by-cycle mode action.
O: Disable
1: Enable
(R/W)

MCPWM_TZn_F0_CBC Configures whether event_f0 will trigger cycle-by-cycle mode action.
O: Disable
1: Enable
(R/W)

MCPWM_TZn_SW_OST Configures whether to enable software force one-shot mode action.
O: Disable
1: Enable
(R/W)

MCPWM_TZn_F2_OST Configures whether event_f2 will trigger one-shot mode action.
O: Disable
1: Enable
(R/W)

MCPWM_TZn_F1_OST Configures whether event_f1 will trigger one-shot mode action.
O: Disable
1: Enable
(R/W)

MCPWM_TZn_Fn_OST Configures whether event_f0 will trigger one-shot mode action.
O: Disable
1: Enable
(R/W)
```