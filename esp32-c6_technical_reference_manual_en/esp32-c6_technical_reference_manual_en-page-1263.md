

```markdown
Chapter 36 Motor Control PWM (MCPWM)  
GoBack

Register 36.40. MCPWM_CARRIER1_CFG_REG (0x009C)

| Bit | Description |
|-----|-------------|
| 31  | (Reserved)  |
| 14  |             |
| 13  |             |
| 12  |             |
| 11  | MCPWM_CARRIER1_IN_INVERT |
| 8   | MCPWM_CARRIER1_OUT_INVERT |
| 7   | MCPWM_CARRIER1_OSHTWTH |
| 5   | MCPWM_CARRIER1_DUTY     |
| 4   | MCPWM_CARRIER1_PRESCALE |
| 1   | MCPWM_CARRIER1_EN       |
| 0   | Reset                   |

MCPWM_CARRIER1_EN Configures whether or not to enable carrier1 function.  
O: Bypass carrier1  
1: Enable carrier1 function  
(R/W)

MCPWM_CARRIER1_PRESCALE Configures the PWM carrier1 clock (PC_CLK) prescale value. Period of PC_CLK = period of PWM_CLK * (PWM_CARRIERO_PRESCALE + 1). (R/W)

MCPWM_CARRIER1_DUTY Configures carrier duty selection. Duty = PWM_CARRIERO_DUTY/8. (R/W)

MCPWM_CARRIER1_OSHTWTH Configures width of the first pulse in number of periods of the carrier. (R/W)

MCPWM_CARRIER1_OUT_INVERT Configures whether or not to invert the output of PWM1A and PWM1B for this submodule.  
O: No effect  
1: Invert  
(R/W)

MCPWM_CARRIER1_IN_INVERT Configures whether or not to invert the input of PWM1A and PWM1B for this submodule.  
O: No effect  
1: Invert  
(R/W)
```