

```markdown
Register 36.26. MCPWM_CARRIERO_CFG_REG (0x0064)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 14  | MCPWM_CARRIERO_IN_INVERT                   | Configures whether or not to invert the input of PWM0A and PWM0B for this submodule. O: No effect<br>1: Invert (R/W) |
| 13  | MCPWM_CARRIERO_OUT_INVERT                  | Configures whether or not to invert the output of PWM0A and PWM0B for this submodule. O: No effect<br>1: Invert (R/W) |
| 12  | MCPWM_CARRIERO_DUTY                        | Configures carrier duty selection. Duty = PWM_CARRIERO_DUTY/8. (R/W)         |
| 11  | MCPWM_CARRIERO_OSHTWH                      | Configures width of the first pulse in number of periods of the carrier. (R/W) |
| 8   | MCPWM_CARRIERO_PRESCALE                    | Configures the prescale value of PWM carrier0 clock (PC_CLK), so that period of PC_CLK = period of PWM_CLK * (PWM_CARRIERO_PRESCALE + 1). (R/W) |
| 7   | MCPWM_CARRIERO_EN                          | Configures whether or not to enable carrier0. O: Bypass<br>1: Enable (R/W)    |
```