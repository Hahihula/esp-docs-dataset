
```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| Monitor configuration registers            |                                                                                                  |         |        |
| ASSIST_DEBUG_CORE_O_MONTR_ENA_REG         | Monitoring enable register                                                                       | 0x0000  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MIN_REG   | Configures boundary address of region 0 monitored on Data bus                                   | 0x0010  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MAX_REG   | Configures boundary address of region 0 monitored on Data bus                                   | 0x0014  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MIN_REG   | Configures boundary address of region 1 monitored on Data bus                                   | 0x0018  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MAX_REG   | Configures boundary address of region 1 monitored on Data bus                                   | 0x001C  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_O_MIN_REG     | Configures boundary address of region 0 monitored on Peripheral bus                            | 0x0020  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_O_MAX_REG     | Configures boundary address of region 0 monitored on Peripheral bus                            | 0x0024  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_1_MIN_REG     | Configures boundary address of region 1 monitored on Peripheral bus                            | 0x0028  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PIF_1_MAX_REG     | Configures boundary address of region 1 monitored on Peripheral bus                            | 0x002C  | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_PC_REG            | Region monitoring PC status register                                                           | 0x0030  | RO     |
| ASSIST_DEBUG_CORE_O_AREA_SP_REG            | Region monitoring SP status register                                                           | 0x0034  | RO     |
| ASSIST_DEBUG_CORE_O_SP_MIN_REG             | Configures stack monitoring boundary address                                                  | 0x0038  | R/W    |
| ASSIST_DEBUG_CORE_O_SP_MAX_REG             | Configures stack monitoring boundary address                                                  | 0x003C  | R/W    |
| ASSIST_DEBUG_CORE_O_SP_PC_REG              | Stack monitoring PC status register                                                           | 0x0040  | RO     |
| Interrupt configuration registers          |                                                                                                  |         |        |
| ASSIST_DEBUG_CORE_O_INTR_RAW_REG           | Interrupt status register                                                                       | 0x0004  | RO     |
```