

```markdown
Register 36.7. MCPWM_TIMER1_CFG1_REG (0x0018)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 5   | MCPWM_TIMER1_MOD            | Configures the working mode of PWM timer1.                                  |
| 4   |                             |                                                                             |
| 3   |                             |                                                                             |
| 2   | MCPWM_TIMER1_START          | Configures conditions to start/stop PWM timer1.                             |
| 1   |                             |                                                                             |
| 0   | Reset                      |                                                                             |

MCPWM_TIMER1_START
Configures conditions to start/stop PWM timer1.
- 0: If PWM timer1 starts, then stops at TEZ
- 1: If timer1 starts, then stops at TEP
- 2: PWM timer1 starts and runs on
- 3: Timer1 starts and stops at the next TEZ
- 4: Timer1 starts and stops at the next TEP
- 5-7: Invalid. No effect

TEP here and below means the event that happens when the timer equals to period.
(R/W/SC)

MCPWM_TIMER1_MOD
Configures the working mode of PWM timer1.
- 0: Freeze
- 1: Increase mode
- 2: Decrease mode
- 3: Up-down mode
(R/W)
```