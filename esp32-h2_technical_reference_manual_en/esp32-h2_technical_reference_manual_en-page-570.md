

# Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)

Register 17.34. ASSIST_DEBUG_CORE_O_DEBUG_MODE_REG (0x0074)

```
31                                 2                 1                 0
+-------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |
+-------------------------------------------------------------------------------------------------+
```

ASSIST_DEBUG_CORE_O_DEBUG_MODE Represents whether ESP-RISC-V CPU is in debugging mode.
1: In debugging mode
0: Not in debugging mode
(RO)

ASSIST_DEBUG_CORE_O_DEBUG_MODULE_ACTIVE Represents the status of the ESP-RISC-V CPU debug module.
1: Active status
Other: Inactive status
(RO)

Register 17.35. ASSIST_DEBUG_CLOCK_GATE_REG (0x0078)

```
31                                 1                 0
+-------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |
+-------------------------------------------------------------------------------------------------+
```

ASSIST_DEBUG_CLK_EN Configures whether to enable the register clock gating.
0: Disable
1: Enable
(R/W)