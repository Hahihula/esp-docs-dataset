

```markdown
Register 36.58. MCPWM_FAULT_DETECT_REG (0x00E4)

| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  |                          | (reserved)                                                                  |
| 9   | MCPWM_EVENT_F2           | Represents the status of fault_event2. This field is set and reset by hardware.<br>0: fault_event2 is not ongoing<br>1: fault_event2 is ongoing (RO) |
| 8   | MCPWM_EVENT_F1           | Represents the status of fault_event1. This field is set and reset by hardware.<br>0: fault_event1 is not ongoing<br>1: fault_event1 is ongoing (RO) |
| 7   | MCPWM_EVENT_F0           | Represents the status of fault_event0. This field is set and reset by hardware.<br>0: fault_event0 is not ongoing<br>1: fault_event0 is ongoing (RO) |
| 6   | MCPWM_F2_POLE            | Configures fault_event2 trigger polarity on FAULT2 source from GPIO matrix.<br>0: Level low<br>1: Level high (R/W) |
| 5   | MCPWM_F1_POLE            | Configures fault_event1 trigger polarity on FAULT1 source from GPIO matrix.<br>0: Level low<br>1: Level high (R/W) |
| 4   | MCPWM_FO_POLE            | Configures fault_event0 trigger polarity on FAULT0 source from GPIO matrix.<br>0: Level low<br>1: Level high (R/W) |
| 3   | MCPWM_F2_EN              | Configures whether or not to enable fault_event2 generation.<br>0: No effect<br>1: Enable (R/W) |
| 2   | MCPWM_F1_EN              | Configures whether or not to enable fault_event1 generation.<br>0: No effect<br>1: Enable (R/W) |
| 1   | MCPWM_FO_EN              | Configures whether or not to enable fault_event0 generation.<br>0: No effect<br>1: Enable (R/W) |
```