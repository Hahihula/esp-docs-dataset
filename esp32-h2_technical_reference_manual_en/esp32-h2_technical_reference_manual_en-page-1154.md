

```markdown
Register 36.68. MCPWM_UPDATE_CFG_REG (0x010C)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                    |                                                                             |
| 30  | MCPWM_GLOBAL_UP_EN          | Configures whether to globally update all active registers.                 |
|     |                             | O: No effect                                                                |
|     |                             | 1: Update all active registers globally (R/W)                               |
| 29  | MCPWM_GLOBAL_FORCE_UP       | Configures whether or not to trigger a forced update of all active registers globally. |
|     |                             | O: No effect                                                                |
|     |                             | 1: Trigger a forced update (R/W)                                            |
| 28  | MCPWM_OPO_UP_EN             | Configures whether or not to update active registers in PWM operator O when MCPWM_GLOBAL_UP_EN is set to 1. |
|     |                             | O: No effect                                                                |
|     |                             | 1: Update active registers in PWM operator O (R/W)                          |
| 27  | MCPWM_OPO_FORCE_UP          | Configures whether or not to trigger a forced update of active registers in PWM operator O. |
|     |                             | O: No effect                                                                |
|     |                             | 1: Trigger a forced update (R/W)                                            |
| 26  | MCPWM_OP1_UP_EN             | Configures whether or not to update active registers in PWM operator 1 when MCPWM_GLOBAL_UP_EN is set to 1. |
|     |                             | O: No effect                                                                |
|     |                             | 1: Update active registers in PWM operator 1 (R/W)                          |

Continued on the next page...
```