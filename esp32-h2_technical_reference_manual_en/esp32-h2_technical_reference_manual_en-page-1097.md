

```markdown
| 31 | (reserved) |
|-----:|:------------|
||5|4|3|2|0|
||O×O|   |   ||Reset|

MCPWM_TIMERO_START Configures conditions to start/stop PWM timer0.
0: If PWM timer0 starts, then stops at TEZ
1: If timer0 starts, then stops at TEP
2: PWM timer0 starts and runs on
3: Timer0 starts and stops at the next TEZ
4: Timer0 starts and stops at the next TEP
5: Invalid. No effect
6: Invalid. No effect
7: Invalid. No effect

TEP here and below means the event that happens when the timer equals to period.
(R/W/SC)

MCPWM_TIMERO_MOD Configures the working mode of PWM timer0.
0: Freeze
1: Increase mode
2: Decrease mode
3: Up-down mode
(R/W)
```