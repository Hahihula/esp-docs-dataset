

```markdown
Register 56.21. MCPWM_FHn_STATUS_REG(n: 0-2) (0x0070+0x38*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| ... |                                                                             |
| 2   | MCPWM_TZn_OST_ON                                                             |
| 1   | MCPWM_TZn_CBC_ON                                                             |
| 0   | Reset                                                                       |

MCPWM_TZn_CBC_ON Represents whether an cycle-by-cycle mode action is on going.
O: No action
1: Ongoing (RO)

MCPWM_TZn_OST_ON Represents whether a one-shot mode action is ongoing.
O: No action
1: Ongoing (RO)

Register 56.22. MCPWM_FAULT_DETECT_REG (0x00E4)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| ... |                                                                             |
| 9   | MCPWM_EVENT_Fn                                                                |
| 8   | MCPWM_POLE                                                                  |
| 7-3 | (reserved)                                                                  |
| 2   | MCPWM_Fn_EN                                                                  |
| 1   | MCPWM_FO_EN                                                                  |
| 0   | Reset                                                                       |

MCPWM_Fn_EN Configures whether to enable event_fn generation.
O: Disable
1: Enable (R/W)

MCPWM_Fn_POLE Configures event_fn trigger polarity on FAULTn source from GPIO matrix.
O: Level low
1: Level high (R/W)

MCPWM_EVENT_Fn Represents whether an event_fn is ongoing. This field is set and reset by hardware.
O: No action
1: Ongoing (RO)
```