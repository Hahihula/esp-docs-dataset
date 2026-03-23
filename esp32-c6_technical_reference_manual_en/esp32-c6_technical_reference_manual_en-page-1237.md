

```markdown
Register 36.11. MCPWM_TIMER2_CFG1_REG (0x0028)

| 31 | (reserved) | MCPWM_TIMER2_MOD | MCPWM_TIMER2_START |
|----:|:-----------|------------------:|--------------------:|
|    |            |                 5 |                     0 |
| 0 | 0 | 0 | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0x0 | Reset |

MCPWM_TIMER2_START Configures whether or not to start/stop PWM timer2.
- 0: If PWM timer2 starts, then stops at TEZ
- 1: If timer2 starts, then stops at TEP
- 2: PWM timer2 starts and runs on
- 3: Timer2 starts and stops at the next TEZ
- 4: Timer2 starts and stops at the next TEP
- 5: Invalid. No effect
- 6: Invalid. No effect
- 7: Invalid. No effect

TEP here and below means the event that happens when the timer equals to period.
(R/W/SC)

MCPWM_TIMER2_MOD Configures the working mode of PWM timer2.
- 0: Freeze
- 1: Increase mode
- 2: Decrease mode
- 3: Up-down mode

(R/W)
```