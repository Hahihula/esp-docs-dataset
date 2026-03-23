

```markdown
Register 10.26. SYSTIMER_INT_ENA_REG (0x0064)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)                    |
| 3   | SYSTIMER_TARGET2_INT_ENA      |
| 2   | SYSTIMER_TARGET1_INT_ENA      |
| 1   | SYSTIMER_TARGET0_INT_ENA      |
| 0   | Reset                         |

SYSTIMER_TARGET0_INT_ENA    SYSTIMER_TARGET0_INT enable bit. (R/W)
SYSTIMER_TARGET1_INT_ENA    SYSTIMER_TARGET1_INT enable bit. (R/W)
SYSTIMER_TARGET2_INT_ENA    SYSTIMER_TARGET2_INT enable bit. (R/W)

Register 10.27. SYSTIMER_INT_RAW_REG (0x0068)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)                    |
| 3   | SYSTIMER_TARGET2_INT_RAW      |
| 2   | SYSTIMER_TARGET1_INT_RAW      |
| 1   | SYSTIMER_TARGET0_INT_RAW      |
| 0   | Reset                         |

SYSTIMER_TARGET0_INT_RAW    SYSTIMER_TARGET0_INT raw bit. (R/WTC/SS)
SYSTIMER_TARGET1_INT_RAW    SYSTIMER_TARGET1_INT raw bit. (R/WTC/SS)
SYSTIMER_TARGET2_INT_RAW    SYSTIMER_TARGET2_INT raw bit. (R/WTC/SS)
```