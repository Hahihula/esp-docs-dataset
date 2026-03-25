

```markdown
| Bit Field                             | Description                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------|
| MCPWM_TIMER2_SYNC_REG                | Register 36.12. MCPWM_TIMER2_SYNC_REG (0x002C)                              |

MCPWM_TIMER2_SYNC_REG (0x002C)

+----+----+----+----+----+----+----+----+----+----+
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 |
+----+----+----+----+----+----+----+----+----+----+
|    |    |    |    |    |    |    |    |    |    |
+----+----+----+----+----+----+----+----+----+----+

MCPWM_TIMER2_SYNC_REG (0x002C)

- MCPWM_TIMER2_SYNC_REG: Configures whether or not to enable timer reloading with phase on sync input event.
  - O: Disable
  - 1: Enable
    (R/W)
- MCPWM_TIMER2_SYNC_SW: Configures whether to trigger a software sync.
  - O: No effect
  - 1: Trigger a software sync
    (R/W)
- MCPWM_TIMER2_SYNC_SEL: Configures PWM timer2 sync out selection.
  - O: sync_in
  - 1: TEZ
  - 2: TEP, and sync out will always generate when toggling the reg_timer0_sync_sw bit
  - 3: No effect
    (R/W)
- MCPWM_TIMER2_PHASE: Configures phase for timer reload on sync event. (R/W)
- MCPWM_TIMER2_PHASE_DIRECTION: Configures the PWM timer2’s direction when timer2 is in up-down mode.
  - O: Increase
  - 1: Decrease
    (R/W)

```
```plaintext
(reserved) MCPWM_TIMER2_PHASE
MCPWM_TIMER2_SYNC_REG (0x002C)
```

```markdown
| Bit Field                             | Description                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------|
| MCPWM_TIMER2_SYNC_REG                | Register 36.12. MCPWM_TIMER2_SYNC_REG (0x002C)                              |

MCPWM_TIMER2_SYNC_REG (0x002C)

+----+----+----+----+----+----+----+----+----+----+
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 |
+----+----+----+----+----+----+----+----+----+----+
|    |    |    |    |    |    |    |    |    |    |
+----+----+----+----+----+----+----+----+----+----+

MCPWM_TIMER2_SYNC_REG (0x002C)

- MCPWM_TIMER2_SYNC_REG: Configures whether or not to enable timer reloading with phase on sync input event.
  - O: Disable
  - 1: Enable
    (R/W)
- MCPWM_TIMER2_SYNC_SW: Configures whether to trigger a software sync.
  - O: No effect
  - 1: Trigger a software sync
    (R/W)
- MCPWM_TIMER2_SYNC_SEL: Configures PWM timer2 sync out selection.
  - O: sync_in
  - 1: TEZ
  - 2: TEP, and sync out will always generate when toggling the reg_timer0_sync_sw bit
  - 3: No effect
    (R/W)
- MCPWM_TIMER2_PHASE: Configures phase for timer reload on sync event. (R/W)
- MCPWM_TIMER2_PHASE_DIRECTION: Configures the PWM timer2’s direction when timer2 is in up-down mode.
  - O: Increase
  - 1: Decrease
    (R/W)

```
```plaintext
(reserved) MCPWM_TIMER2_PHASE
MCPWM_TIMER2_SYNC_REG (0x002C)
```