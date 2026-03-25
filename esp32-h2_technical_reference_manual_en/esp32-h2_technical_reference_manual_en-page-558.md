

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)
Register 17:13. ASSIST_DEBUG_CORE_O_MONTR_ENA_REG (0x0000)

Continued from the previous page...

ASSIST_DEBUG_CORE_O_AREA_PIF_O_WR_ENA Configures whether to monitor write operations in region 0 by the peripheral bus.
O: Not Monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_ENA Configures whether to monitor read operations in region 1 by the peripheral bus.
O: Not Monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_ENA Configures whether to monitor write operations in region 1 by the peripheral bus.
O: Not Monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_ENA Configures whether to monitor SP less than the starting address of SP monitored region.
O: Not Monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_ENA Configures whether to monitor SP greater than the ending address of SP monitored region.
O: Not Monitor
1: Monitor
(R/W)
```