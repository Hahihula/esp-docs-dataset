

```markdown
Register 36.15. MCPWM_OPERATOR_TIMERSSEL_REG (0x0038)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | Reset                                                                       |
|     |                                                                             |
| 6   | MCPWM_OPERATOR2_TIMERSSEL                                                  |
| 5   | MCPWM_OPERATOR1_TIMERSSEL                                                  |
| 4   | MCPWM_OPERATOR0_TIMERSSEL                                                  |
| 3   | (reserved)                                                                 |
| 2   | (reserved)                                                                 |
| 1   | (reserved)                                                                 |
| 0   | (reserved)                                                                 |

```markdown
MCPWM_OPERATOR0_TIMERSSEL Configures which PWM timer will be the timing reference for PWM operator0.
```

- O: timer0
- 1: timer1
- 2: timer2
- 3: Invalid

(R/W)

```markdown
MCPWM_OPERATOR1_TIMERSSEL Configures which PWM timer will be the timing reference for PWM operator1.
```

- O: timer0
- 1: timer1
- 2: timer2
- 3: Invalid

(R/W)

```markdown
MCPWM_OPERATOR2_TIMERSSEL Configures which PWM timer will be the timing reference for PWM operator2.
```

- O: timer0
- 1: timer1
- 2: timer2
- 3: Invalid

(R/W)
```