

```markdown
| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 5   | MCPWM_TIMER2_MOD                    | Configures the working mode of PWM timer2. <br> 0: Freeze <br> 1: Increase mode <br> 2: Decrease mode <br> 3: Up-down mode (R/W) |
| 4   | MCPWM_TIMER2_START                  | Configures whether or not to start/stop PWM timer2. <br> 0: If PWM timer2 starts, then stops at TEZ <br> 1: If timer2 starts, then stops at TEP <br> 2: PWM timer2 starts and runs on <br> 3: Timer2 starts and stops at the next TEZ <br> 4: Timer2 starts and stops at the next TEP <br> 5: Invalid. No effect <br> 6: Invalid. No effect <br> 7: Invalid. No effect <br> TEP here and below means the event that happens when the timer equals to period. (R/W/SC) |
| 3   | MCPWM_TIMER2_MOD                    |                                                                             |
| 2   | MCPWM_TIMER2_START                  |                                                                             |
| 1   | Reset                               |                                                                             |
```