

```markdown
## 17.6 Registers

The addresses in this section are relative to Debug Assistant base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 171: ASSIST_DEBUG_CORE_O_MONTR_ENA_REG (0x0000)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_RD_ENA Monitoring enable bit for read operations in region 0 by the Data bus. (R/W)
ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_WR_ENA Monitoring enable bit for write operations in region 0 by the Data bus. (R/W)
ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_ENA Monitoring enable bit for read operations in region 1 by the Data bus. (R/W)
ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_ENA Monitoring enable bit for write operations in region 1 by the Data bus. (R/W)
ASSIST_DEBUG_CORE_O_AREA_PIF_O_RD_ENA Monitoring enable bit for read operations in region 0 by the Peripheral bus. (R/W)
ASSIST_DEBUG_CORE_O_AREA_PIF_O_WR_ENA Monitoring enable bit for write operations in region 0 by the Peripheral bus. (R/W)
ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_ENA Monitoring enable bit for read operations in region 1 by the Peripheral bus. (R/W)
ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_ENA Monitoring enable bit for write operations in region 1 by the Peripheral bus. (R/W)
ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_ENA Monitoring enable bit for SP exceeding the lower bound address of SP monitored region. (R/W)
ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_ENA Monitoring enable bit for SP exceeding the upper bound address of SP monitored region. (R/W)
```