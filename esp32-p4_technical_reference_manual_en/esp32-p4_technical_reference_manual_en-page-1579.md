

# 34.12 Registers

## 34.12.1 HUK Registers

The addresses in this section are relative to HUK base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section IX .

### Register 34.1. HUK_CLK_REG (0x0004)

```
31
+---------------------------------------------------------------+
| (reserved)                                                   | 2   1   0 |
|                                                             | Reset |
+---------------------------------------------------------------+
| HUK_CLK_EN    Configures whether or not to force on register clock gate.
|               0: Not force on
|               1: Force on
|               (R/W)
|
| HUK_MEM_CG_FORCE_ON Configures whether or not to force on memory clock gate.
|               0: Not force on
|               1: Force on
|               (R/W)
```

### Register 34.2. HUK_INT_RAW_REG (0x0008)

```
31
+---------------------------------------------------------------+
| (reserved)                                                   | 3   2   1   0 |
|                                                             | Reset |
+---------------------------------------------------------------+
| HUK_PREP_DONE_INT_RAW The raw interrupt status of HUK_PREP_DONE_INT interrupt.
|                        (RO/WTC/SS)
|
| HUK_PROC_DONE_INT_RAW The raw interrupt status of HUK_PROC_DONE_INT interrupt.
|                        (RO/WTC/SS)
|
| HUK_POST_DONE_INT_RAW The raw interrupt status of HUK_POST_DONE_INT interrupt.
|                        (RO/WTC/SS)
```