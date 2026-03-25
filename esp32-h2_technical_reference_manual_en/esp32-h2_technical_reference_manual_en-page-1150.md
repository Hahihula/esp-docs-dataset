

```markdown
Register 36.61. MCPWM_CAP_CH0_CFG_REG (0x00F0)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | MCPWM_CAP0_EN                                                                |
| 29  | MCPWM_CAP0_MODE                                                              |
| 28  | MCPWM_CAP0_PRESCALE                                                          |
| 27  | MCPWM_CAP0_IN_INVERT                                                         |
| 26  | MCPWM_CAP0_SW                                                                 |
| 25  | MCPWM_CAP0_CH0_CFG_REG                                                      |

MCPWM_CAP0_EN Configures whether or not to enable capture on channel O.
- 0: Not enable
- 1: Enable
(R/W)

MCPWM_CAP0_MODE Configures the edge of capture on channel O after prescaling.
When bit0 is set to 1: enable capture on the falling edge.
When bit1 is set to 1: enable capture on the rising edge.
(R/W)

MCPWM_CAP0_PRESCALE Configures the prescale value on the rising edge of CAPO. Prescale
value = PWM_CAPO_PRESCALE + 1. (R/W)

MCPWM_CAP0_IN_INVERT Configures whether or not to invert the CAPO from GPIO matrix before
prescale.
- 0: No effect
- 1: Invert
(R/W)

MCPWM_CAP0_SW Configures whether or not to trigger a software-forced capture on channel O.
- 0: Not trigger
- 1: Trigger
(WT)
```