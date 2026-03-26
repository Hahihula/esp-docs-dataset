

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Fault Detection Configuration and Status** |                                                                             |           |        |
| MCPWM_FAULT_DETECT_REG                     | Fault detection configuration and status                                   | 0x00E4    | varies |
| **Capture Configuration and Status**       |                                                                             |           |        |
| MCPWM_CAP_TIMER_CFG_REG                    | Configure capture timer                                                     | 0x00E8    | varies |
| MCPWM_CAP_TIMER_PHASE_REG                  | Phase for capture timer sync                                                | 0x00EC    | R/W    |
| MCPWM_CAP_CHO_CFG_REG                      | Capture channel 0 configuration and enable                                  | 0x00F0    | varies |
| MCPWM_CAP_CH1_CFG_REG                      | Capture channel 1 configuration and enable                                  | 0x00F4    | varies |
| MCPWM_CAP_CH2_CFG_REG                      | Capture channel 2 configuration and enable                                  | 0x00F8    | varies |
| MCPWM_CAP_CHO_REG                          | ch0 capture value status register                                           | 0x00FC    | RO     |
| MCPWM_CAP_CH1_REG                          | ch1 capture value status register                                           | 0x0100    | RO     |
| MCPWM_CAP_CH2_REG                          | ch2 capture value status register                                           | 0x0104    | RO     |
| MCPWM_CAP_STATUS_REG                       | Edge of last capture trigger                                                | 0x0108    | RO     |
| **Enable Update of Active Registers**       |                                                                             |           |        |
| MCPWM_UPDATE_CFG_REG                       | Enable update                                                               | 0x010C    | R/W    |
| **Manage Interrupts**                      |                                                                             |           |        |
| MCPWM_INT_ENA_REG                          | Interrupt enable bits                                                       | 0x0110    | R/W    |
| MCPWM_INT_RAW_REG                          | Raw interrupt status                                                        | 0x0114    | R/WTC /SS |
| MCPWM_INT_ST_REG                           | Masked interrupt status                                                     | 0x0118    | RO     |
| MCPWM_INT_CLR_REG                          | Interrupt clear bits                                                        | 0x011C    | WT     |
| **MCPWM Event Enable Registers**           |                                                                             |           |        |
| MCPWM_EVT_EN_REG                           | MCPWM event enable register                                                 | 0x0120    | R/W    |
| MCPWM_EVT_EN2_REG                          | MCWM event enable register2                                                 | 0x0128    | R/W    |
| **MCPWM Task Enable Register**             |                                                                             |           |        |
| MCPWM_TASK_EN_REG                          | MCPWM task enable register                                                  | 0x0124    | R/W    |
| **MCPWM Generator Configuration Registers**|                                                                             |           |        |
| MCPWM_OPO_TSTMP_E1_REG                     | Generator0 time stamp E1 value configuration register                      | 0x012C    | R/W    |
| MCPWM_OPO_TSTMP_E2_REG                     | Generator0 time stamp E2 value configuration register                      | 0x0130    | R/W    |
| MCPWM_OP1_TSTMP_E1_REG                     | Generator1 time stamp E1 value configuration register                      | 0x0134    | R/W    |
| MCPWM_OP1_TSTMP_E2_REG                     | Generator1 time stamp E2 value configuration register                      | 0x0138    | R/W    |
| MCPWM_OP2_TSTMP_E1_REG                     | Generator2 time stamp E1 value configuration register                      | 0x013C    | R/W    |
| MCPWM_OP2_TSTMP_E2_REG                     | Generator2 time stamp E2 value configuration register                      | 0x0140    | R/W    |
| **MCPWM APB Configuration Register**       |                                                                             |           |        |
| MCPWM_CLK_REG                              | MCPWM APB configuration register                                            | 0x0144    | R/W    |
| **Version Register**                       |                                                                             |           |        |
| MCPWM_VERSION_REG                          | Version control register                                                    | 0x0148    | R/W    |
```