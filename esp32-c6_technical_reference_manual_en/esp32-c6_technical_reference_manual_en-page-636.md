

# Chapter 18 Debug Assistant (ASSIST_DEBUG)

## Register 18.34. ASSIST_DEBUG_CORE_O_DEBUG_MODE_REG (0x0074)

```
31                                 2   1   0
+-----------------------------------------------+
| (reserved) | ASSIST_DEBUG_CORE_O_DEBUG_MODULE_ACTIVE | ASSIST_DEBUG_CORE_O_DEBUG_MODE |
+-----------------------------------------------+
|                 Reset                            |
+-----------------------------------------------+
```

**ASSIST_DEBUG_CORE_O_DEBUG_MODE** Represents whether RISC-V CPU (HP CPU) is in debugging mode.  
1: In debugging mode  
0: Not in debugging mode  
(RO)

**ASSIST_DEBUG_CORE_O_DEBUG_MODULE_ACTIVE** Represents the status of the RISC-V CPU (HP CPU) debug module.  
1: Active status  
Other: Inactive status  
(RO)

## Register 18.35. ASSIST_DEBUG_CLOCK_GATE_REG (0x0078)

```
31                                 1   0
+-----------------------------------------------+
| (reserved) | ASSIST_DEBUG_CLK_EN |
+-----------------------------------------------+
|                 Reset                            |
+-----------------------------------------------+
```

**ASSIST_DEBUG_CLK_EN** Configures whether to enable the register clock gating.  
0: Disable  
1: Enable  
(R/W)

Espressif Systems

636
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback