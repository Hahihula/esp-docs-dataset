

```markdown
| Bit Field                  | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| MCPWM_TIMER2_SYNC_EN      | Configures whether or not to enable timer reloading with phase on sync input event. <br> 0: Disable <br> 1: Enable (R/W) |
| MCPWM_TIMER2_SYNC_SW      | Toggling this bit will trigger a software sync. (R/W)                       |
| MCPWM_TIMER2_SYNC_SEL     | PWM timer2 sync out selection. <br> 0: sync_in <br> 1: TEZ <br> 2: TEP, and sync out will always generate when toggling the reg_timer0_sync_sw bit <br> 3: No effect (R/W) |
| MCPWM_TIMER2_PHASE         | Configures phase for timer reload on sync event. (R/W)                      |
| MCPWM_TIMER2_PHASE_DIRECTION | Configures the PWM timer2’s direction when timer2 is in up-down mode. <br> 0: Increase <br> 1: Decrease (R/W) |
```