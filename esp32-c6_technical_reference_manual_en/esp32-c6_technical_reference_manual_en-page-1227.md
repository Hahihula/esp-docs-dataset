

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| Prescaler Configuration                   |                                                                              |           |        |
| MCPWM_CLK_CFG_REG                         | PWM clock prescaler register                                                                   | 0x0000    | R/W    |
| MCPWM Timer 0 Configuration and Status    |                                                                              |           |        |
| MCPWM_TIMERO_CFG0_REG                     | PWM timer0 period and update method config-uration register                                    | 0x0004    | R/W    |
| MCPWM_TIMERO_CFG1_REG                     | PWM timer0 working mode and start/stop con-trol configuration register                        | 0x0008    | varies |
| MCPWM_TIMERO_SYNC_REG                     | PWM timer0 sync function configuration regis-ter                                              | 0x000C    | R/W    |
| MCPWM_TIMERO_STATUS_REG                   | PWM timer0 status register                                                                      | 0x0010    | RO     |
| MCPWM Timer 1 Configuration and Status    |                                                                              |           |        |
| MCPWM_TIMER1_CFG0_REG                     | PWM timer1 period and update method config-uration register                                    | 0x0014    | R/W    |
| MCPWM_TIMER1_CFG1_REG                     | PWM timer1 working mode and start/stop con-trol configuration register                        | 0x0018    | varies |
| MCPWM_TIMER1_SYNC_REG                     | PWM timer1 sync function configuration register                                                | 0x001C    | R/W    |
| MCPWM_TIMER1_STATUS_REG                   | PWM timer1 status register                                                                      | 0x0020    | RO     |
| MCPWM Timer 2 Configuration and Status    |                                                                              |           |        |
| MCPWM_TIMER2_CFG0_REG                     | PWM timer2 period and update method config-uration register                                    | 0x0024    | R/W    |
| MCPWM_TIMER2_CFG1_REG                     | PWM timer2 working mode and start/stop con-trol configuration register                        | 0x0028    | varies |
| MCPWM_TIMER2_SYNC_REG                     | PWM timer2 sync function configuration regis-ter                                              | 0x002C    | R/W    |
| MCPWM_TIMER2_STATUS_REG                   | PWM timer2 status register                                                                      | 0x0030    | RO     |
| Common Configuration for MCPWM Timers      |                                                                              |           |        |
| MCPWM_TIMER_SYNCNCF_CFG_REG               | Synchronization input selection for three PWM timers                                          | 0x0034    | R/W    |
| MCPWM_OPERATOR_TIMERSL_REG                | Select specific timer for PWM operators                                                        | 0x0038    | R/W    |
| MCPWM Operator 0 Configuration and Status |                                                                              |           |        |
| MCPWM_GENOSTMP_CFG_REG                    | Transfer status and update method for time stamp registers A and B                             | 0x003C    | varies |
| MCPWM_GENOTSTMP_A_REG                     | Shadow register for register A                                                                  | 0x0040    | R/W    |
| MCPWM_GENOTSTMP_B_REG                     | Shadow register for register B                                                                  | 0x0044    | R/W    |
| MCPWM_GENOCFGO_REG                        | Fault event TO and T1 handling                                                                  | 0x0048    | R/W    |
| MCPWM_GENOFORCE_REG                       | Permissives to force PWMOA and PWMOB out-puts by software                                     | 0x004C    | R/W    |
```