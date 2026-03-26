

```markdown
Register 15.26. SYSTIMER_INT_ENA_REG (0x0064)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   |   | Reset |

SYSTIMER_TARGETO_INT_ENA Write 1 to enable SYSTIMER_TARGETO_INT. (R/W)
SYSTIMER_TARGET1_INT_ENA Write 1 to enable SYSTIMER_TARGET1_INT. (R/W)
SYSTIMER_TARGET2_INT_ENA Write 1 to enable SYSTIMER_TARGET2_INT. (R/W)

Register 15.27. SYSTIMER_INT_RAW_REG (0x0068)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   |   | Reset |

SYSTIMER_TARGETO_INT_RAW The raw interrupt status of SYSTIMER_TARGETO_INT. (R/WTC/SS)
SYSTIMER_TARGET1_INT_RAW The raw interrupt status of SYSTIMER_TARGET1_INT. (R/WTC/SS)
SYSTIMER_TARGET2_INT_RAW The raw interrupt status of SYSTIMER_TARGET2_INT. (R/WTC/SS)
```