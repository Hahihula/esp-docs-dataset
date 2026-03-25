

```markdown
Register 41.4. MCPWM_TIMERn_SYNC_REG (n: 0-2) (0x000C+0x10*n)
```

| Bit Field | Description |
|-----------|-------------|
| 31        | (reserved) |
| 30-29     | MCPWM_TIMERn_PHASE_DIRECTION Configures the PWM timer's direction when timer mode is up-down mode. O: Increase<br>1: Decrease<br>(R/W) |
| 28-27     | MCPWM_TIMERn_PHASE Configures the phase for timer reload on sync event.<br>(R/W) |
| 26         | MCPWM_TIMERn_SYNC_SEL Configures PWM timer sync out selection. O: sync_in. The sync out will always generate when toggling the MCPWM_TIMERn_SYNC_SW bit.<br>1: TEZ<br>2: TEP<br>3: No effect<br>(R/W) |
| 25         | MCPWM_TIMERn_SYNC_SW Configures whether to trigger a software sync.<br>O: No effect<br>1: Trigger a software sync<br>(R/W) |
| 24-0      | MCPWM_TIMERn_SYNC_EN Configures whether to enable timer reloading with phase on sync input event.<br>O: Disable<br>1: Enable<br>(R/W) |

```markdown
MCPWM_TIMERn_SYNC_REG (n: 0-2)
```

```plaintext
31          21   20   19            4    3    2    1    0
+-----------+------+------+------+------+------+------+------
| (reserved)|      | MCPWM_TIMERn_PHASE_DIRECTION | Reset |
+-----------+------+------+------+------+------+------+------
| O         | O     |                               |       |
```

```markdown
MCPWM_TIMERn_SYNC_EN Configures whether to enable timer reloading with phase on sync input event.
O: Disable
1: Enable
(R/W)
```

```markdown
MCPWM_TIMERn_SYNC_SW Configures whether to trigger a software sync.
O: No effect
1: Trigger a software sync
(R/W)
```

```markdown
MCPWM_TIMERn_SYNC_SEL Configures PWM timer sync out selection.
O: sync_in. The sync out will always generate when toggling the MCPWM_TIMERn_SYNC_SW bit.
1: TEZ
2: TEP
3: No effect
(R/W)
```

```markdown
MCPWM_TIMERn_PHASE Configures the phase for timer reload on sync event.
(R/W)
```

```markdown
MCPWM_TIMERn_PHASE_DIRECTION Configures the PWM timer's direction when timer mode is up-down mode.
O: Increase
1: Decrease
(R/W)
```
```