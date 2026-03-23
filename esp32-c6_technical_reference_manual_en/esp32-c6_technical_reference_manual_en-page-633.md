

```markdown
| Bit | Name                                 | Description                                                                                                                                                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                                                                                                                                                             |
| 30  | ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_CLR | Write 1 to clear the interrupt for SP exceeding the upper bound address of SP monitored region. (R/W)                                                                                                         |
| 29  | ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_CLR | Write 1 to clear the interrupt for SP exceeding the lower bound address of SP monitored region. (R/W)                                                                                                         |
| 28  | ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_CLR | Write 1 to clear the interrupt for write operations in region 1 by Peripheral bus. (R/W)                                                                                                                     |
| 27  | ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_CLR | Write 1 to clear the interrupt for read operations in region 1 by Peripheral bus. (R/W)                                                                                                                     |
| 26  | ASSIST_DEBUG_CORE_O_AREA_PIF_0_WR_CLR | Write 1 to clear the interrupt for write operations in region 0 by Peripheral bus. (R/W)                                                                                                                     |
| 25  | ASSIST_DEBUG_CORE_O_AREA_PIF_0_RD_CLR | Write 1 to clear the interrupt for read operations in region 0 by Peripheral bus. (R/W)                                                                                                                     |
| 24  | ASSIST_DEBUG_CORE_O_DRAMO_1_WR_CLR    | Write 1 to clear the interrupt for write operations in region 1 by Data bus. (R/W)                                                                                                                           |
| 23  | ASSIST_DEBUG_CORE_O_DRAMO_1_RD_CLR    | Write 1 to clear the interrupt for read operations in region 1 by Data bus. (R/W)                                                                                                                           |
| 22  | ASSIST_DEBUG_CORE_O_DRAMO_0_WR_CLR    | Write 1 to clear the interrupt for write operations in region 0 by Data bus. (R/W)                                                                                                                           |
| 21  | ASSIST_DEBUG_CORE_O_DRAMO_0_RD_CLR    | Write 1 to clear the interrupt for read operations in region 0 by Data bus. (R/W)                                                                                                                           |
```

Register 18.29. ASSIST_DEBUG_CORE_O_INTR_CLR_REG (0x000C)
ASSIST_DEBUG_CORE_O_AREA_DRAMO_0_RD_CLR Write 1 to clear the interrupt for read operations in region 0 by Data bus. (R/W)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_0_WR_CLR Write 1 to clear the interrupt for write operations in region 0 by Data bus. (R/W)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_CLR Write 1 to clear the interrupt for read operations in region 1 by Data bus. (R/W)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_CLR Write 1 to clear the interrupt for write operations in region 1 by Data bus. (R/W)

ASSIST_DEBUG_CORE_O_AREA_PIF_0_RD_CLR Write 1 to clear the interrupt for read operations in region 0 by Peripheral bus. (R/W)

ASSIST_DEBUG_CORE_O_AREA_PIF_0_WR_CLR Write 1 to clear the interrupt for write operations in region 0 by Peripheral bus. (R/W)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_CLR Write 1 to clear the interrupt for read operations in region 1 by Peripheral bus. (R/W)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_CLR Write 1 to clear the interrupt for write operations in region 1 by Peripheral bus. (R/W)

ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_CLR Write 1 to clear the interrupt for SP exceeding the lower bound address of SP monitored region. (R/W)

ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_CLR Write 1 to clear the interrupt for SP exceeding the upper bound address of SP monitored region. (R/W)
```