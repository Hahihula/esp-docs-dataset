

```markdown
Register 36.41. MCPWM_FH1_CFG0_REG (0x00AAO)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 24  | MCPWM_FH1_B_OST_U                    |                                                                             |
| 23  | MCPWM_FH1_B_OST_D                    |                                                                             |
| 22  | MCPWM_FH1_B_CBC_U                    |                                                                             |
| 21  | MCPWM_FH1_B_CBC_D                    |                                                                             |
| 20  | MCPWM_FH1_A_OST_U                    |                                                                             |
| 19  | MCPWM_FH1_A_OST_D                    |                                                                             |
| 18  | MCPWM_FH1_A_CBC_U                    |                                                                             |
| 17  | MCPWM_FH1_A_CBC_D                    |                                                                             |
| 16  | MCPWM_FH1_SW_CBC_U                   |                                                                             |
| 15  | MCPWM_FH1_SW_CBC_D                   |                                                                             |
| 14  | MCPWM_FH1_F2_OST                     |                                                                             |
| 13  | MCPWM_FH1_F2_OST                     |                                                                             |
| 12  | MCPWM_FH1_F2_CBC_U                   |                                                                             |
| 11  | MCPWM_FH1_F2_CBC_D                   |                                                                             |
| 10  | MCPWM_FH1_F1_OST                     |                                                                             |
| 9   | MCPWM_FH1_F1_OST                     |                                                                             |
| 8   | MCPWM_FH1_F1_CBC_U                   |                                                                             |
| 7   | MCPWM_FH1_F1_CBC_D                   |                                                                             |
| 6   | MCPWM_FH1_SW_OST                     |                                                                             |
| 5   | MCPWM_FH1_SW_OST                     |                                                                             |
| 4   | Reset                                |                                                                             |
| 3   | 0                                   |                                                                             |
| 2   | 0                                   |                                                                             |
| 1   | 0                                   |                                                                             |
| 0   | 0                                   |                                                                             |

MCPWM_FH1_SW_CBC Configures whether or not to enable software force cycle-by-cycle mode action.
O: Disable
1: Enable
(R/W)

MCPWM_FH1_F2_CBC Configures whether or not fault_event2 will trigger cycle-by-cycle mode action.
O: Disable
1: Enable
(R/W)

MCPWM_FH1_F1_CBC Configures whether or not fault_event1 will trigger cycle-by-cycle mode action. See details in MCPWM_FH1_F2_CBC. (R/W)

MCPWM_FH1_F0_CBC Configures whether or not fault_event0 will trigger cycle-by-cycle mode action. See details in MCPWM_FH1_F2_CBC. (R/W)

MCPWM_FH1_SW_OST Configures whether or not to enable register for software force one-shot mode action. See details in MCPWM_FH1_SW_CBC. (R/W)

MCPWM_FH1_F2_OST Configures whether or not fault_event2 will trigger one-shot mode action. See details in MCPWM_FH1_F2_CBC. (R/W)

MCPWM_FH1_F1_OST Configures whether or not fault_event1 will trigger one-shot mode action. See details in MCPWM_FH1_F2_CBC. (R/W)

MCPWM_FH1_F0_OST Configures whether or not fault_event0 will trigger one-shot mode action. See details in MCPWM_FH1_F2_CBC. (R/W)

MCPWM_FH1_A_CBC_D Configures cycle-by-cycle mode action on PWM1A when fault event occurs and timer is decreasing.
O: Do nothing
1: Force low
2: Force high
3: Toggle
(R/W)

MCPWM_FH1_A_CBC_U Configures cycle-by-cycle mode action on PWM1A when fault event occurs and timer is increasing. See details in MCPWM_FH1_F2_CBC. (R/W)
```