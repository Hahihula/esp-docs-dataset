

```markdown
Chapter 18 Debug Assistant (ASSIST_DEBUG)

GoBack

18.6.2 Other Registers

Register 18.13. ASSIST_DEBUG_CORE_O_MONTR_ENA_REG (0x0000)
```

![Register Bit Field Diagram](image_description: A bit field diagram for register 0x0000 labeled "ASSIST_DEBUG_CORE_O_MONTR_ENA_REG" showing bits from 31 to 0. Bits are grouped and labeled as follows:
- Bits 31–24: reserved
- Bit 23: ASSIST_DEBUG_CORE_O_SP_SPILL_MAX_ENA
- Bit 22: ASSIST_DEBUG_CORE_O_SP_SPILL_MIN_ENA
- Bit 21: ASSIST_DEBUG_CORE_O_AREA_PIF_1_WR_ENA
- Bit 20: ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_ENA
- Bit 19: ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_ENA
- Bit 18: ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_ENA
- Bits 17–8: reserved
- Bit 7: ASSIST_DEBUG_CORE_O_AREA_DRAMO_0_WR_ENA
- Bit 6: ASSIST_DEBUG_CORE_O_AREA_DRAMO_0_RD_ENA
- Bits 5–0: reserved)

```markdown
ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_RD_ENA Configures whether to monitor read operations in region 0 by the Data bus.
O: Not monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_WR_ENA Configures whether to monitor write operations in region 0 by the Data bus.
O: Not monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_ENA Configures whether to monitor read operations in region 1 by the Data bus.
O: Not Monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_ENA Configures whether to monitor write operations in region 1 by the Data bus.
O: Not Monitor
1: Monitor
(R/W)

ASSIST_DEBUG_CORE_O_AREA_PIF_O_RD_ENA Configures whether to monitor read operations in region 0 by the Peripheral bus.
O: Not Monitor
1: Monitor
(R/W)
```

Continued on the next page...

Espressif Systems

623

ESP32-C6 TRM (Version 1.1)

Submit Documentation Feedback
```