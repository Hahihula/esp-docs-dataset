
```markdown
Register 36.9. MCPWM_TIMER1_STATUS_REG (0x0020)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             |                                                                             |
| 17  |                             |                                                                             |
| 16  |                             |                                                                             |
| 15  | MCPWM_TIMER1_DIRECTION      | Represents current PWM timer1 counter direction.                           |
|     |                             | 0: Increment                                                                  |
|     |                             | 1: Decrement                                                                  |
| (RO)|                             |                                                                             |
| 0   | MCPWM_TIMER1_VALUE          | Represents current PWM timer1 counter value. (RO)                          |

Register 36.10. MCPWM_TIMER2_CFG0_REG (0x0024)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             |                                                                             |
| 26  |                             |                                                                             |
| 25  |                             |                                                                             |
| 24  |                             |                                                                             |
| 23  |                             |                                                                             |
|     | MCPWM_TIMER2_PERIOD         | Period shadow register of PWM timer2. (R/W)                                 |
|     |                             |                                                                             |
|     | MCPWM_TIMER2_PERIOD_UPMETHOD| Configures the update method for active register of PWM timer2 period.      |
|     |                             | 0: Immediate                                                                  |
|     |                             | 1: TEZ                                                                        |
|     |                             | 2: Sync                                                                       |
|     |                             | 3: TEZ | sync                                                                         |
| (R/W)|                             | TEZ here and below means timer equal zero event.                            |

MCPWM_TIMER2_PRESCALE Configures the prescaler value of timer2, so that the period of PTO_CLK = Period of PWM_CLK * (PWM_timer2_PRESCALE + 1). (R/W)
```