

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
|MCPWM_GEN0_A_REG                            | Actions triggered by events on PWMOA                                                             | 0x0050    | R/W    |
|MCPWM_GEN0_B_REG                            | Actions triggered by events on PWMOB                                                             | 0x0054    | R/W    |
|MCPWM_DTO_CFG_REG                           | Dead time type selection and configuration                                                     | 0x0058    | R/W    |
|MCPWM_DTO_FED_CFG_REG                       | Shadow register for falling edge delay (FED)                                                    | 0x005C    | R/W    |
|MCPWM_DTO_RED_CFG_REG                       | Shadow register for rising edge delay (RED)                                                     | 0x0060    | R/W    |
|MCPWM_CARRIER0_CFG_REG                      | Carrier enable and configuration                                                                | 0x0064    | R/W    |
|MCPWM_FHO_CFG0_REG                          | Actions on PWMOA and PWMOB trip events                                                          | 0x0068    | R/W    |
|MCPWM_FHO_CFG1_REG                          | Software triggers for fault handler actions                                                     | 0x006C    | R/W    |
|MCPWM_FHO_STATUS_REG                        | Status of fault events                                                                           | 0x0070    | RO     |

MCPWM Operator 1 Configuration and Status
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
|MCPWM_GEN1_STMP_CFG_REG                     | Transfer status and update method for time stamp registers A and B                               | 0x0074    | varies |
|MCPWM_GEN1_TSTMP_A_REG                      | Shadow register for register A                                                                  | 0x0078    | R/W    |
|MCPWM_GEN1_TSTMP_B_REG                      | Shadow register for register B                                                                  | 0x007C    | R/W    |
|MCPWM_GEN1_CFG0_REG                         | Fault event T0 and T1 handling                                                                   | 0x0080    | R/W    |
|MCPWM_GEN1_FORCE_REG                        | Permissives to force PWM1A and PWM1B outputs by software                                        | 0x0084    | R/W    |

| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
|MCPWM_GEN1_A_REG                            | Actions triggered by events on PWM1A                                                             | 0x0088    | R/W    |
|MCPWM_GEN1_B_REG                            | Actions triggered by events on PWM1B                                                             | 0x008C    | R/W    |
|MCPWM_DT1_CFG_REG                           | Dead time type selection and configuration                                                     | 0x0090    | R/W    |
|MCPWM_DT1_FED_CFG_REG                       | Shadow register for falling edge delay (FED)                                                    | 0x0094    | R/W    |
|MCPWM_DT1_RED_CFG_REG                       | Shadow register for rising edge delay (RED)                                                     | 0x0098    | R/W    |
|MCPWM_CARRIER1_CFG_REG                      | Carrier enable and configuration                                                                | 0x009C    | R/W    |
|MCPWM_FH1_CFG0_REG                          | Actions on PWM1A and PWM1B trip events                                                          | 0x00A0    | R/W    |
|MCPWM_FH1_CFG1_REG                          | Software triggers for fault handler actions                                                     | 0x00A4    | R/W    |
|MCPWM_FH1_STATUS_REG                        | Status of fault events                                                                           | 0x00A8    | RO     |

MCPWM Operator 2 Configuration and Status
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
|MCPWM_GEN2_STMP_CFG_REG                     | Transfer status and update method for time stamp registers A and B                               | 0x00AC    | varies |
|MCPWM_GEN2_TSTMP_A_REG                      | Shadow register for register A                                                                  | 0x00B0    | R/W    |
|MCPWM_GEN2_TSTMP_B_REG                      | Shadow register for register B                                                                  | 0x00B4    | R/W    |
|MCPWM_GEN2_CFG0_REG                         | Fault event T0 and T1 handling                                                                   | 0x00B8    | R/W    |
|MCPWM_GEN2_FORCE_REG                        | Permissives to force PWM2A and PWM2B outputs by software                                        | 0x00BC    | R/W    |

| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
|MCPWM_GEN2_A_REG                            | Actions triggered by events on PWM2A                                                             | 0x00C0    | R/W    |
|MCPWM_GEN2_B_REG                            | Actions triggered by events on PWM2B                                                             | 0x00C4    | R/W    |
|MCPWM_DT2_CFG_REG                           | Dead time type selection and configuration                                                     | 0x00C8    | R/W    |
|MCPWM_DT2_FED_CFG_REG                       | Shadow register for falling edge delay (FED)                                                    | 0x00CC    | R/W    |
|MCPWM_DT2_RED_CFG_REG                       | Shadow register for rising edge delay (RED)                                                     | 0x00D0    | R/W    |
|MCPWM_CARRIER2_CFG_REG                      | Carrier enable and configuration                                                                | 0x00D4    | R/W    |
|MCPWM_FH2_CFG0_REG                          | Actions on PWM2A and PWM2B trip events                                                          | 0x00D8    | R/W    |
|MCPWM_FH2_CFG1_REG                          | Software triggers for fault handler actions                                                     | 0x00DC    | R/W    |
|MCPWM_FH2_STATUS_REG                        | Status of fault events                                                                           | 0x00E0    | RO     |
```