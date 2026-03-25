

```markdown
Chapter 36 Motor Control PWM (MCPWM) GoBack


Register 36.4. MCPWM_TIMERO_SYNC_REG (0x000C)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 21-20 | MCPWM_TIMERO_PHASE_DIRECTION |
| 19   | MCPWM_TIMERO_PHASE |
| 4    | MCPWM_TIMERO_SYNC_SEL |
| 3    | MCPWM_TIMERO_SYNC_SW |
| 2    | MCPWM_TIMERO_SYNCI_EN |
| Reset|             |

MCPWM_TIMERO_SYNCI_EN Configures whether or not to enable timer reloading with phase on sync input event.
O: Disable
1: Enable
(R/W)

MCPWM_TIMERO_SYNC_SW Configures whether to trigger a software sync.
O: No effect
1: Trigger a software sync
(R/W)

MCPWM_TIMERO_SYNC_SEL Configures PWM timer1 sync out selection.
O: sync_in. The sync out will always generate when toggling the MCPWM_TIMERO_SYNC_SW bit.
1: TEZ
2: TEP
3: No effect
(R/W)

MCPWM_TIMERO_PHASE Configures the phase for timer reload on sync event. (R/W)

MCPWM_TIMERO_PHASE_DIRECTION Configures the PWM timer0's direction when timer0 mode is up-down mode.
O: Increase
1: Decrease
(R/W)
```