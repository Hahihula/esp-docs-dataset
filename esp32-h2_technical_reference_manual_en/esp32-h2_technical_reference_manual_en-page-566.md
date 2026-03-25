

```markdown
| Address bits | Description |
|--------------|-------------|
| 31           | reserved     |
|              |             |
| 30-29        | ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_INTR_ENA Write 1 to enable the interrupt for SP greater than the ending address of SP monitored region. (R/W) |
| 28-27        | ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_INTR_ENA Write 1 to enable the interrupt for SP less than the starting address of SP monitored region. (R/W) |
| 26           | ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_INTR_ENA Write 1 to enable the interrupt for write operations in region 1 by peripheral bus. (R/W) |
| 25           | ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_INTR_ENA Write 1 to enable the interrupt for read operations in region 1 by peripheral bus. (R/W) |
| 24-23        | ASSIST_DEBUG_CORE_O_AREA_PIF_O_WR_INTR_ENA Write 1 to enable the interrupt for write operations in region 0 by peripheral bus. (R/W) |
| 22           | ASSIST_DEBUG_CORE_O_AREA_PIF_O_RD_INTR_ENA Write 1 to enable the interrupt for read operations in region 0 by peripheral bus. (R/W) |
| 21-20        | ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_INTR_ENA Write 1 to enable the interrupt for write operations in region 1 by data bus. (R/W) |
| 19           | ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_INTR_ENA Write 1 to enable the interrupt for read operations in region 1 by data bus. (R/W) |
| 18-17        | ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_WR_INTR_ENA Write 1 to enable the interrupt for write operations in region 0 by data bus. (R/W) |
| 16           | ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_RD_INTR_ENA Write 1 to enable the interrupt for read operations in region 0 by data bus. (R/W) |
```