

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)
```

Register 17.20. ASSIST_DEBUG_CORE_O_AREA_PIF_1_MIN_REG (0x0028)

| 31 | 0 |
|----|---|
| Oxffffffff | Reset |

ASSIST_DEBUG_CORE_O_AREA_PIF_1_MIN Configures the starting address of peripheral bus region 1. (R/W)

Register 17.21. ASSIST_DEBUG_CORE_O_AREA_PIF_1_MAX_REG (0x002C)

| 31 | 0 |
|----|---|
| 0 | Reset |

ASSIST_DEBUG_CORE_O_AREA_PIF_1_MAX Configures the ending address of peripheral bus region 1. (R/W)

Register 17.22. ASSIST_DEBUG_CORE_O_AREA_PC_REG (0x0030)

| 31 | 0 |
|----|---|
| 0 | Reset |

ASSIST_DEBUG_CORE_O_AREA_PC Represents the PC value when an interrupt is triggered during region monitoring. (RO)
```