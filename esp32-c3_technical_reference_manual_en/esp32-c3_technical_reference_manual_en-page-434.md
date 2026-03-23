

# 16.5 Registers

The addresses below are relative to the base address of system register provided in Table 3.3-3 in Chapter 3 *System and Memory*.

## Register 16.1. SYSTEM_CPU_PERI_CLK_EN_REG (0x0000)

```
30
+---------------------------------------------------------------+
| 7 | 6 | 5 | ... | 0 |
+---------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset |
+---------------------------------------------------------------+
```

SYSTEM_CLK_EN_ASSIST_DEBUG Set this bit to enable the ASSIST_DEBUG clock. Please see Chapter 17 Debug Assistant (ASSIST_DEBUG) for more information about ASSIST_DEBUG. (R/W)

## Register 16.2. SYSTEM_CPU_PERI_RST_EN_REG (0x0004)

```
31
+---------------------------------------------------------------+
| 8 | 7 | 6 | ... | 0 |
+---------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0 0 0 0 0 Reset |
+---------------------------------------------------------------+
```

SYSTEM_RST_EN_ASSIST_DEBUG Set this bit to reset the ASSIST_DEBUG clock. Please see Chapter 17 Debug Assistant (ASSIST_DEBUG) for more information about ASSIST_DEBUG. (R/W)