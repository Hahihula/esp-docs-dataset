

```markdown
| Name                                 | Description                          | Address | Access |
|--------------------------------------|--------------------------------------|---------|--------|
| MEM_MONITOR_DATESS_REG               | Version control register             | 0x03FC  | R/W    |

## 20.6.2 Summary of Other Registers

| Name                                                                                       | Description                                                                                   | Address | Access |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|---------|--------|
| **Monitor configuration registers**                                                     |                                                                              |         |        |
| BUS_MONITOR_CORE_O_MONTR_ENA_REG                                                      | Configures whether to enable HP CPU monitoring                                              | 0x0000  | R/W    |
| BUS_MONITOR_CORE_O_AREA_DRAMO_O_MIN_REG                                               | Configures lower boundary address of region 0 monitored on Data bus                         | 0x0010  | R/W    |
| BUS_MONITOR_CORE_O_AREA_DRAMO_O_MAX_REG                                               | Configures upper boundary address of region 0 monitored on Data bus                         | 0x0014  | R/W    |
| BUS_MONITOR_CORE_O_AREA_DRAMO_1_MIN_REG                                                | Configures lower boundary address of region 1 monitored on Data bus                         | 0x0018  | R/W    |
| BUS_MONITOR_CORE_O_AREA_DRAMO_1_MAX_REG                                                | Configures upper boundary address of region 1 monitored on Data bus                         | 0x001C  | R/W    |
| BUS_MONITOR_CORE_O_AREA_PIF_O_MIN_REG                                                  | Configures lower boundary address of region 0 monitored on Peripheral bus                  | 0x0020  | R/W    |
| BUS_MONITOR_CORE_O_AREA_PIF_O_MAX_REG                                                  | Configures upper boundary address of region 0 monitored on Peripheral bus                  | 0x0024  | R/W    |
| BUS_MONITOR_CORE_O_AREA_PIF_1_MIN_REG                                                  | Configures lower boundary address of region 1 monitored on Peripheral bus                  | 0x0028  | R/W    |
| BUS_MONITOR_CORE_O_AREA_PIF_1_MAX_REG                                                  | Configures upper boundary address of region 1 monitored on Peripheral bus                  | 0x002C  | R/W    |
| BUS_MONITOR_CORE_O_AREA_PC_REG                                                          | Represents the PC status under HP CPU region monitoring                                    | 0x0030  | RO     |
| BUS_MONITOR_CORE_O_AREA_SP_REG                                                          | Represents the SP status under HP CPU region monitoring                                    | 0x0034  | RO     |
| BUS_MONITOR_CORE_O_SP_MIN_REG                                                           | Configures SP monitoring lower boundary address                                            | 0x0038  | R/W    |
| BUS_MONITOR_CORE_O_SP_MAX_REG                                                           | Configures SP monitoring upper boundary address                                            | 0x003C  | R/W    |
| BUS_MONITOR_CORE_O_SP_PC_REG                                                             | Represents the PC status under HP CPU/SP monitoring                                        | 0x0040  | RO     |
| **Interrupt configuration registers**                                                   |                                                                              |         |        |
| BUS_MONITOR_CORE_O_INTR_RAW_REG                                                         | HP CPU monitor raw interrupt status register                                               | 0x0004  | RO     |
| BUS_MONITOR_CORE_O_INTR_ENA_REG                                                         | HP CPU monitor interrupt enable register                                                   | 0x0008  | R/W    |
| BUS_MONITOR_CORE_O_INTR_CLR_REG                                                         | HP CPU monitor interrupt clear register                                                    | 0x000C  | WT     |
| **PC recording configuration register**                                                 |                                                                              |         |        |
| BUS_MONITOR_CORE_O_RCD_EN_REG                                                           | HP CPU PC logging enable register                                                           | 0x0044  | R/W    |
| **PC recording status registers**                                                       |                                                                              |         |        |
| BUS_MONITOR_CORE_O_RCD_PDEBUGPC_REG                                                     | HP CPU PC logging register                                                                  | 0x0048  | RO     |
```