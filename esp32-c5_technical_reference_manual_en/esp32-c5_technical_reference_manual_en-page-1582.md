

```markdown
Register 41.18. MCPWM_CARRIERn_CFG_REG(n: 0-2) (0x0064+0x38*n)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30  | MCPWM_CHOPPERn_EN                   | Configures whether to enable carrier n.                                    |
|     |                                      | 0: Bypassed                                                                  |
|     |                                      | 1: Enabled                                                                   |
|     | (R/W)                               |                                                                             |
| 29  | MCPWM_CHOPPERn_PRESCALE             | Configures the prescale value of PWM carrier n clock (PC_clk), so that period of PC_clk = period of PWM_clk * (PWM_CARRIERn_PRESCALE + 1). (R/W) |
| 28  | MCPWM_CHOPPERn_DUTY                 | Configures carrier duty. Duty = PWM_CARRIERn_DUTY / 8. (R/W)                  |
| 27  | MCPWM_CHOPPERn_OSTHWTH              | Configures width of the first pulse. Measurement unit: Periods of the carrier. (R/W) |
| 26  | MCPWM_CHOPPERn_OUT_INVERT           | Configures whether to invert the output of PWMn A and PWMn B for this submodule. |
|     |                                      | 0: Normal                                                                     |
|     |                                      | 1: Invert                                                                      |
|     | (R/W)                               |                                                                             |
| 25  | MCPWM_CHOPPERn_IN_INVERT            | Configures whether to invert the input of PWMn A and PWMn B for this submodule. |
|     |                                      | 0: Normal                                                                     |
|     |                                      | 1: Invert                                                                      |
|     | (R/W)                               |                                                                             |

Reset values:
Bit 31-25: 0
Bit 24: 0
Bit 23-22: 0
Bit 21-20: 0
Bit 19-18: 0
Bit 17-16: 0
Bit 15-14: 0
Bit 13-12: 0
Bit 11-10: 0
Bit 9-8: 0
Bit 7-6: 0
Bit 5-4: 0
Bit 3-2: 0
Bit 1-0: 0
```