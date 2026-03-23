

```markdown
Register 36.58. MCPWM_FAULT_DETECT_REG (0x00E4)

| Bit | Name                        | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 31  |                              | (reserved)                                                                  |
| 9   | MCPWM_EVENT_F2               |                                                                             |
| 8   | MOPWM_EVENT_F1               |                                                                             |
| 7   | MOPWM_EVENT_F0               |                                                                             |
| 6   | MCPWM_F2_POLE                |                                                                             |
| 5   | MCPWM_F1_POLE                |                                                                             |
| 4   | MCPWM_F0_POLE                |                                                                             |
| 3   | MCPWM_F1_EN                  |                                                                             |
| 2   | MCPWM_F2_EN                  |                                                                             |
| 1   | MCPWM_F0_EN                  |                                                                             |
| 0   | Reset                        |                                                                             |

MCPWM_F0_EN Configures whether or not to enable fault_event0 generation.
O: No effect
1: Enable
(R/W)

MCPWM_F1_EN Configures whether or not to enable fault_event1 generation.
O: No effect
1: Enable
(R/W)

MCPWM_F2_EN Configures whether or not to enable fault_event2 generation.
O: No effect
1: Enable
(R/W)

MCPWM_F0_POLE Configures fault_event0 trigger polarity on FAULT0 source from GPIO matrix.
O: Level low
1: Level high
(R/W)

MCPWM_F1_POLE Configures fault_event1 trigger polarity on FAULT1 source from GPIO matrix.
O: Level low
1: Level high
(R/W)

MCPWM_F2_POLE Configures fault_event2 trigger polarity on FAULT2 source from GPIO matrix.
O: Level low
1: Level high
(R/W)

MCPWM_EVENT_F0 Represents set and reset by hardware. If set, fault_event0 is on going. (RO)
MCPWM_EVENT_F1 Represents set and reset by hardware. If set, fault_event1 is on going. (RO)
MCPWM_EVENT_F2 Represents set and reset by hardware. If set, fault_event2 is on going. (RO)
```