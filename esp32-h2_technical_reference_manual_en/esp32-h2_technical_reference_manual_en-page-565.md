

```markdown
| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_RAW                                       |
| 29  | ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_RAW                                       |
| 28  | ASSIST_DEBUG_CORE_O_PIF_1_WR_RAW                                           |
| 27  | ASSIST_DEBUG_CORE_O_PIF_1_RD_RAW                                           |
| 26  | ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_RAW                                      |
| 25  | ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_RAW                                      |
| 24  | ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_RAW                                    |
| 23  | ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_RAW                                    |
| 22  | ASSIST_DEBUG_CORE_O_AREA_DRAMO_0_WR_RAW                                    |
| 21  | ASSIST_DEBUG_CORE_O_AREA_DRAMO_0_RD_RAW                                    |
| Reset| 0                                                                            |
```

ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_RD_RAW The raw interrupt status of read operations in region 0 by data bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_WR_RAW The raw interrupt status of write operations in region 0 by data bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_RAW The raw interrupt status of read operations in region 1 by data bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_RAW The raw interrupt status of write operations in region 1 by data bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_PIF_O_RD_RAW The raw interrupt status of read operations in region 0 by peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_PIF_O_WR_RAW The raw interrupt status of write operations in region 0 by peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_RAW The raw interrupt status of read operations in region 1 by peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_RAW The raw interrupt status of write operations in region 1 by peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_RAW The raw interrupt status of SP less than the starting address of SP monitored region. (RO)

ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_RAW The raw interrupt status of SP greater than the ending address of SP monitored region. (RO)
```