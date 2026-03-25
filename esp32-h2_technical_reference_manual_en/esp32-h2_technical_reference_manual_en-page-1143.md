

```markdown
| Bit Field                     | Description                                                                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCPWM_CARRIER2_EN            | Configures whether or not to enable the carrier2 function. <br> 0: Bypass carrier2 <br> 1: Enable <br> (R/W)                                                                                               |
| MCPWM_CARRIER2_PRESCALE      | Configures the PWM carrier2 clock (PC_CLK) prescale value. Period of PC_CLK = period of PWM_CLK * (PWM_CARRIER0_PRESCALE + 1). (R/W)                                                                         |
| MCPWM_CARRIER2_DUTY          | Configures the carrier duty selection. Duty = PWM_CARRIER0_DUTY/8. <br> (R/W)                                                                                                                               |
| MCPWM_CARRIER2_OSHTWTH       | Configures the width of the first pulse in number of periods of the carrier. (R/W)                                                                                                                                 |
| MCPWM_CARRIER2_OUT_INVERT    | Configures whether or not to invert the output of PWM2A and PWM2B for this submodule. <br> 0: No effect <br> 1: Invert <br> (R/W)                                                                                   |
| MCPWM_CARRIER2_IN_INVERT     | Configures whether or not to invert the input of PWM2A and PWM2B for this submodule. <br> 0: No effect <br> 1: Invert <br> (R/W)                                                                               |
```