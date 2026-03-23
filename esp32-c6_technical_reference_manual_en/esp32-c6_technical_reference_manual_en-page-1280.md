

```markdown
Register 36.59. MCPWM_CAP_TIMER_CFG_REG (0x00E8)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 30-24|                             | (reserved)                                                                  |
| 23  | MCPWM_CAP_SYNC_SW           | Configures whether or not to enable capture timer sync under APB_CLK.       |
| 22  | MCPWM_CAP_SYNCI_SEL         | Configures the capture module sync input selection:                         |
|     |                             | - 0: None                                                                   |
|     |                             | - 1: timer0 sync out                                                        |
|     |                             | - 2: timer1 sync out                                                        |
|     |                             | - 3: timer2 sync out                                                        |
|     |                             | - 4: SYNC0 from GPIO matrix                                                 |
|     |                             | - 5: SYNC1 from GPIO matrix                                                 |
|     |                             | - 6: SYNC2 from GPIO matrix                                                 |
| (R/W)| MCPWM_CAP_TIMER_EN          | Configures whether or not to enable capture timer incrementing under APB_CLK.|
|     |                             | - 0: No effect                                                              |
|     |                             | - 1: Enable                                                                 |
| (R/W)| MCPWM_CAP_SYNCI_EN          | Configures whether or not to enable capture timer sync.                     |
|     |                             | - 0: No effect                                                              |
|     |                             | - 1: Enable                                                                 |

Register 36.60. MCPWM_CAP_TIMER_PHASE_REG (0x00EC)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
|     |                             | Reset                                                                      |
|     | MCPWM_CAP_PHASE             | Configures the phase value for capture timer sync operation.                |
```