

```markdown
|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|| ||ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_RAW||ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_RAW||ASSIST_DEBUG_CORE_O_PIF_1_WR_RAW||ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_RAW||ASSIST_DEBUG_CORE_O_PIF_O_WR_RAW||ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_WR_RAW||ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_RD_RAW||reserved|
```

ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_RD_RAW Interrupt status bit for read operations in region 0 by the Data bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_WR_RAW Interrupt status bit for write operations in region 0 by the Data bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_RAW Interrupt status bit for read operations in region 1 by the Data bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_RAW Interrupt status bit for write operations in region 1 by the Data bus. (RO)

ASSIST_DEBUG_CORE_O_PIF_O_RD_RAW Interrupt status bit for read operations in region 0 by the Peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_PIF_O_WR_RAW Interrupt status bit for write operations in region 0 by the Peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_RAW Interrupt status bit for read operations in region 1 by the Peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_RAW Interrupt status bit for write operations in region 1 by the Peripheral bus. (RO)

ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_RAW Interrupt status bit for SP exceeding the lower bound address of SP monitored region. (RO)

ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_RAW Interrupt status bit for SP exceeding the upper bound address of SP monitored region. (RO)
```