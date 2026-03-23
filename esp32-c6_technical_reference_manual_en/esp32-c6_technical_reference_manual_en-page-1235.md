

```markdown
Register 36.8. MCPWM_TIMER1_SYNC_REG (0x01C)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 21  | MCPWM_TIMER1_SYNC_EN                | Configures whether or not to enable timer reloading with phase on sync input event.<br>0: Disable<br>1: Enable<br>(R/W) |
| 20  | MCPWM_TIMER1_SYNC_SW                | Toggling this bit will trigger a software sync. (R/W)                        |
| 19  | MCPWM_TIMER1_SYNCO_SEL              | Configures PWM timer1 sync out selection.<br>0: sync_in<br>1: TEZ<br>2: TEP, and sync out will always generate when toggling the reg_timer1_sync_sw bit.<br>3: No effect<br>(R/W) |
| 4   | MCPWM_TIMER1_PHASE                  | Phase for timer reload on sync event. (R/W)                                 |
| 3   | MCPWM_TIMER1_PHASE_DIRECTION        | Configures the PWM timer1's direction when timer1 is in up-down mode.<br>0: Increase<br>1: Decrease<br>(R/W) |
```