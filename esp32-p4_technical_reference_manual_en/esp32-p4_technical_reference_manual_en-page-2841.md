

```markdown
Register 56.3. MCPWM_TIMERn_CFG1_REG(n: 0-2) (0x0008+0x10*n)

| bit | 31 | ... | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|-----|---|---|---|---|---|---|
|     |    | (reserved) | MCPWM_TIMERn_MOD | MCPWM_TIMERn_START | Reset |

MCPWM_TIMERn_START Configures conditions to start/stop PWM timer n.
- 0: If PWM timer0 starts, then stops at TEZ
- 1: If timer0 starts, then stops at TEP
- 2: PWM timer0 starts and runs on
- 3: Timer0 starts and stops at the next TEZ
- 4: Timer0 starts and stops at the next TEP
- 5: Invalid. No effect
- 6: Invalid. No effect
- 7: Invalid. No effect

TEP here and below means the event that happens when the timer equals to period.
(R/W/SC)

MCPWM_TIMERn_MOD Configures the working mode of PWM timer n.
- 0: Freeze
- 1: Increase mode
- 2: Decrease mode
- 3: Up-down mode

(R/W)
```