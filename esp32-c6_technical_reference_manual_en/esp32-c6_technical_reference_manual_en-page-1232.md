

```markdown
Chapter 36 Motor Control PWM (MCPWM)
GoBack

Register 36.4. MCPWM_TIMERO_SYNC_REG (0x000C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 21  | MCPWM_TIMERO_PHASE                                                          |
| 20  | MCPWM_TIMERO_PHASE_DIRECTION                                                |
| 19  | MCPWM_TIMERO_SYNC_SW                                                        |
| 4   | MCPWM_TIMERO_SYNC_SEL                                                       |
| 3   | MCPWM_TIMERO_SYNC_EN                                                        |
| 2   | (reserved)                                                                  |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                      |

MCPWM_TIMERO_SYNC_EN Configures whether or not to enable timer reloading with phase on sync input event.
O: Disable
1: Enable
(R/W)

MCPWM_TIMERO_SYNC_SW Toggling this bit will trigger a software sync. (R/W)

MCPWM_TIMERO_SYNC_SEL PWM timer0 sync out selection.
O: sync_in. The sync out will always generate when toggling the MCPWM_TIMERO_SYNC_SW bit.
1: TEZ
2: TEP
3: No effect
(R/W)

MCPWM_TIMERO_PHASE Phase for timer reload on sync event. (R/W)

MCPWM_TIMERO_PHASE_DIRECTION Configures the PWM timer0's direction when timer0 mode is up-down mode.
O: Increase
1: Decrease
(R/W)
```