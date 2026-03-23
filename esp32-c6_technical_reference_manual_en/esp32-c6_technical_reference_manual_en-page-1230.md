

```markdown
## 36.5 Registers

The addresses in this section are relative to Motor Control PWM base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 36.1. MCPWM_CLK_CFG_REG (0x0000)

| Bit 31 | ... | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|---|---|---|---|
|        |     |   |   |   |   |   |   |   | (reserved) | MCPWM_CLK_PRESCALE |
| Reset: | Ox0 |    |    |    |    |    |    |    |              |

**MCPWM_CLK_PRESCALE** Configures the prescaler value of clock, so that the period of PWM_CLK = 6.25ns * (PWM_CLK_PRESCALE + 1). (R/W)

### Register 36.2. MCPWM_TIMERO_CFG0_REG (0x0004)

| Bit 31 | ... | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|---|
|        |     |    |    |    | (reserved) | MCPWM_TIMERO_PERIOD_UPMETHOD | MCPWM_TIMERO_PERIOD | MCPWM_TIMERO_PRESCALE |
| Reset: | Ox0 | 0xff |      |      |              |

**MCPWM_TIMERO_PRESCALE** Configures the prescaler value of timer0, so that the period of PTO_CLK = Period of PWM_CLK * (PWM_TIMERO_PRESCALE + 1). (R/W)

**MCPWM_TIMERO_PERIOD** Configures the period shadow register of PWM timer0. (R/W)

**MCPWM_TIMERO_PERIOD_UPMETHOD** Configures the update method for active register of PWM timer0 period.
- 0: Immediate
- 1: TEZ
- 2: sync
- 3: TEZ | sync

TEZ here and below means timer equal zero event.

(R/W)
```