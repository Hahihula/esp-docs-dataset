

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| ASSIST_DEBUG_CORE_1_AREA_PIF_O_MAX_REG    | Configures the upper bound address of region 0 monitored on HP CPU1 Peripheral bus             | 0x00A4    | R/W    |
| ASSIST_DEBUG_CORE_1_AREA_PIF_1_MIN_REG    | Configures the lower bound address of region 1 monitored on HP CPU1 Peripheral bus             | 0x00A8    | R/W    |
| ASSIST_DEBUG_CORE_1_AREA_PIF_1_MAX_REG    | Configures the upper bound address of region 1 monitored on HP CPU1 Peripheral bus             | 0x00AC    | R/W    |
| ASSIST_DEBUG_CORE_1_AREA_PC_REG            | Represents the PC status under HP CPU1 region monitoring                                       | 0x00B0    | RO     |
| ASSIST_DEBUG_CORE_1_AREA_SP_REG            | Represents the SP status under HP CPU1 region monitoring                                       | 0x00B4    | RO     |
| ASSIST_DEBUG_CORE_1_SP_MIN_REG             | Configures the lower bound address of the HP CPU1 SP monitored region                         | 0x00B8    | R/W    |
| ASSIST_DEBUG_CORE_1_SP_MAX_REG             | Configures the upper bound address of the HP CPU1 SP monitored region                         | 0x00BC    | R/W    |
| ASSIST_DEBUG_CORE_1_SP_PC_REG              | Represents the PC status under HP CPU1 SP monitoring                                          | 0x00C0    | RO     |
| Interrupt configuration registers                                                           |                                                                                                  |           |        |
| ASSIST_DEBUG_CORE_O_INTR_RAW_REG           | HP CPUO raw interrupt status register                                                          | 0x0004    | RO     |
| ASSIST_DEBUG_CORE_O_INTR_ENA_REG           | HP CPUO interrupt enable register                                                              | 0x0008    | R/W    |
| ASSIST_DEBUG_CORE_O_INTR_CLR_REG           | HP CPUO interrupt clear register                                                               | 0x000C    | WT     |
| ASSIST_DEBUG_CORE_1_INTR_RAW_REG           | HP CPU1 raw interrupt status register                                                         | 0x0084    | RO     |
| ASSIST_DEBUG_CORE_1_INTR_ENA_REG           | HP CPU1 interrupt enable register                                                              | 0x0088    | R/W    |
| ASSIST_DEBUG_CORE_1_INTR_CLR_REG           | HP CPU1 interrupt clear register                                                               | 0x008C    | WT     |
| PC logging configuration register                                                            |                                                                                                  |           |        |
| ASSIST_DEBUG_CORE_O_RCD_EN_REG             | HP CPUO PC logging enable register                                                             | 0x0044    | R/W    |
| ASSIST_DEBUG_CORE_1_RCD_EN_REG             | HP CPU1 PC logging enable register                                                             | 0x00C4    | R/W    |
| PC logging status registers                                                                   |                                                                                                  |           |        |
| ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG       | HP CPUO PC logging register                                                                    | 0x0048    | RO     |
| ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG       | HP CPUO SP logging register                                                                    | 0x004C    | RO     |
| ASSIST_DEBUG_CORE_1_RCD_PDEBUGPC_REG       | HP CPU1 PC logging register                                                                    | 0x00C8    | RO     |
| ASSIST_DEBUG_CORE_1_RCD_PDEBUGSP_REG       | HP CPU1 SP logging register                                                                    | 0x00CC    | RO     |
| CPU status registers                                                                            |                                                                                                  |           |        |
| ASSIST_DEBUG_CORE_O_LASTPC_BEFORE_EXCEPTION_REG | PC of the last command before HP CPUO enters exception                                       | 0x0070    | RO     |
```