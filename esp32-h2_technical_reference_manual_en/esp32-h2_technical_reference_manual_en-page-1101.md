

```markdown
Register 36.8. MCPWM_TIMER1_SYNC_REG (0x01C)
```

| Bit Field | Description |
|-----------|-------------|
| 31-21     | (reserved) |
| 20        | MCPWM_TIMER1_PHASE_DIRECTION |
| 19        | MCPWM_TIMER1_PHASE |
| 4         | MCPWM_TIMER1_SYNC_SW |
| 3         | MCPWM_TIMER1_SYNC_SEL |
| 2         | MCPWM_TIMER1_SYNC_OSEL |
| 1-0       | Reset |

```markdown
MCPWM_TIMER1_SYNCO_EN Configures whether or not to enable timer reloading with phase on sync input event.
```
O: Disable  
1: Enable  
(R/W)

```markdown
MCPWM_TIMER1_SYNC_SW Configures whether to trigger a software sync.
```
O: No effect  
1: Trigger a software sync  
(R/W)

```markdown
MCPWM_TIMER1_SYNCO_SEL Configures PWM timer1 sync out selection.
```
O: sync_in  
1: TEZ  
2: TEP, and sync out will always generate when toggling the reg_timer1_sync_sw bit.  
3: No effect  
(R/W)

```markdown
MCPWM_TIMER1_PHASE Phase for timer reload on sync event. (R/W)
```

```markdown
MCPWM_TIMER1_PHASE_DIRECTION Configures the PWM timer1's direction when timer1 is in up-down mode.
```
O: Increase  
1: Decrease  
(R/W)
```