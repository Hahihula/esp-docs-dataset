

```markdown
| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                 |                                                                             |
| 13  | MCPWM_CAP1_SW              | Configures whether or not to trigger a software forced capture on channel 1. O: Not trigger<br>1: Trigger (WT) |
| 12  | MCPWM_CAP1_IN_INVERT       | Configures whether or not to invert the CAP1 from GPIO matrix before prescale.<br>O: No effect<br>1: Invert (R/W) |
| 11  | MCPWM_CAP1_PRESCALE        | Configures the value of prescaling on the rising edge of CAP1. Prescale value = PWM_CAP1_PRESCALE + 1. (R/W) |
| 10  | MCPWM_CAP1_MODE            | Configures the edge of capture on channel 1 after prescaling.<br>When bit0 is set to 1: enable capture on the falling edge.<br>When bit1 is set to 1: enable capture on the rising edge. (R/W) |
| 9   | MCPWM_CAP1_EN              | Configures whether or not to enable capture on channel 1.<br>O: Not enable<br>1: Enable (R/W) |
```