

```markdown
## 36.5 Registers

The addresses in this section are relative to Motor Control PWM base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 36.1. MCPWM_CLK_CFG_REG (0x0000)

| Bit | Description         |
|-----|---------------------|
| 31  | reserved            |
| ... |                     |
| 8   | MCPWM_CLK_PRESCALE  |
| 7-0 | OxF                 |

**MCPWM_CLK_PRESCALE**: Configures the prescaler value of clock, so that the period of PWM_CLK = 6.25ns * (PWM_CLK_PRESCALE + 1). (R/W)

### Register 36.2. MCPWM_TIMERO_CFG0_REG (0x0004)

| Bit | Description                              |
|-----|------------------------------------------|
| 31  | reserved                                 |
| ... |                                          |
| 26  | MCPWM_TIMERO_PERIOD_UPMETHOD            |
| 25-24| MCPWM_TIMERO_PERIOD                     |
| 23  | MCPWM_TIMERO_PRESCALE                   |
| 8   | Oxff                                     |
| 7-0 | OxF                                     |

**MCPWM_TIMERO_PRESCALE**: Configures the prescaler value of timer0, so that the period of PTO_CLK = Period of PWM_CLK * (PWM_TIMERO_PRESCALE + 1). (R/W)

**MCPWM_TIMERO_PERIOD**: Configures the period shadow register of PWM timer0. (R/W)

**MCPWM_TIMERO_PERIOD_UPMETHOD**: Configures the update method for active register of PWM timer0 period.
- 0: Immediate
- 1: TEZ
- 2: sync
- 3: TEZ | sync

TEZ here and below means timer equals zero event.

(R/W)
```