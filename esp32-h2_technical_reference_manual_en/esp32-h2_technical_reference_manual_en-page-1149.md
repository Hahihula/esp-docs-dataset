

```markdown
Register 36.59. MCPWM_CAP_TIMER_CFG_REG (0x00E8)

| bit | field name                     | description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30-24|                                | (reserved)                                                                  |
| 23  | MCPWM_CAP_SYNC_SW             | Configures whether or not to enable capture timer sync so that capture timer is loaded with value in phase register. O: No effect<br>1: Trigger a capture timer sync<br>(WT) |
| 22  | MCPWM_CAP_SYNCI_SEL           | Configures the capture module sync input selection.<br>O: None<br>1: timer0 sync out<br>2: timer1 sync out<br>3: timer2 sync out<br>4: SYNC0 from GPIO matrix<br>5: SYNC1 from GPIO matrix<br>6: SYNC2 from GPIO matrix<br>(R/W) |
| 21  | MCPWM_CAP_SYNCI_EN            | Configures whether or not to enable capture timer sync.<br>O: No effect<br>1: Enable<br>(R/W) |
| 20-16|                                | (reserved)                                                                  |
| 15  | MCPWM_CAP_TIMER_EN            | Configures whether or not to enable capture timer incrementing under APB_CLK.<br>O: No effect<br>1: Enable<br>(R/W) |

Register 36.60. MCPWM_CAP_TIMER_PHASE_REG (0x00EC)

| bit | field name                     | description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30-0 | MCPWM_CAP_PHASE              | Configures the phase value for capture timer sync operation. (R/W)          |
```