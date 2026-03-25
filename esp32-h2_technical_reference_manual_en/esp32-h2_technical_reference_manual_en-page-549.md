

```markdown
| Name                                       | Description                                                                                   | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|---------|--------|
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MAX_REG   | Configures the ending address of region 0 monitored on data bus                             | 0x0014  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MIN_REG   | Configures the starting address of region 1 monitored on data bus                            | 0x0018  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MAX_REG   | Configures the ending address of region 1 monitored on data bus                             | 0x001C  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_O_MIN_REG     | Configures the starting address of region 0 monitored on peripheral bus                     | 0x0020  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_O_MAX_REG     | Configures the ending address of region 0 monitored on peripheral bus                       | 0x0024  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_1_MIN_REG     | Configures the starting address of region 1 monitored on peripheral bus                     | 0x0028  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_1_MAX_REG     | Configures the ending address of region 1 monitored on peripheral bus                       | 0x002C  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PC_REG            | Region monitoring CPU PC status register                                                     | 0x0030  | RO     |
| ASSIST_DEBUG_CORE_O_AREA_SP_REG            | Region monitoring CPU SP status register                                                    | 0x0034  | RO     |
| ASSIST_DEBUG_CORE_O_SP_MIN_REG             | Configures the starting address of stack monitored region                                  | 0x0038  | R/W    |
| ASSIST_DEBUG_CORE_O_SP_MAX_REG             | Configures the ending address of stack monitored region                                    | 0x003C  | R/W    |
| ASSIST_DEBUG_CORE_O_SP_PC_REG              | Stack monitoring CPU PC status register                                                     | 0x0040  | RO     |
| Interrupt configuration registers                                                           |                                                                                               |         |        |
| ASSIST_DEBUG_CORE_O_INTR_RAW_REG           | Interrupt status register                                                                    | 0x0004  | RO     |
| ASSIST_DEBUG_CORE_O_INTR_ENA_REG           | Interrupt enable register                                                                    | 0x0008  | R/W    |
| ASSIST_DEBUG_CORE_O_INTR_CLR_REG           | Interrupt clear register                                                                     | 0x000C  | R/W    |
| PC logging configuration register                                                           |                                                                                               |         |        |
| ASSIST_DEBUG_CORE_O_RCD_EN_REG             | CPU PC logging enable register                                                              | 0x0044  | R/W    |
| PC logging status registers                                                                   |                                                                                               |         |        |
| ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG        | PC logging register                                                                          | 0x0048  | RO     |
| ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG        | PC logging register                                                                          | 0x004C  | RO     |
| CPU status registers                                                                            |                                                                                               |         |        |
```