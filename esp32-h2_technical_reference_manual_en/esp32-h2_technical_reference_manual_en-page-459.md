

```markdown
Chapter 12 System Timer (SYSTIMER)  
GoBack

Register 12.26. SYSTIMER_INT_ENA_REG (0x0064)

| Bit 31 | ... | Bit 2 | Bit 1 | Bit 0 | Description |
|--------|-----|-------|-------|-------|-------------|
| 0      | ... | 0     | 0     | 0     | (reserved)  |
|        |     | Reset |       |       |             |

SYSTIMER_TARGETO_INT_ENA Write 1 to enable SYSTIMER_TARGETO_INT. (R/W)
SYSTIMER_TARGET1_INT_ENA Write 1 to enable SYSTIMER_TARGET1_INT. (R/W)
SYSTIMER_TARGET2_INT_ENA Write 1 to enable SYSTIMER_TARGET2_INT. (R/W)

Register 12.27. SYSTIMER_INT_RAW_REG (0x0068)

| Bit 31 | ... | Bit 2 | Bit 1 | Bit 0 | Description |
|--------|-----|-------|-------|-------|-------------|
| 0      | ... | 0     | 0     | 0     | (reserved)  |
|        |     | Reset |       |       |             |

SYSTIMER_TARGETO_INT_RAW The raw interrupt status of SYSTIMER_TARGETO_INT. (R/WTC/SS)
SYSTIMER_TARGET1_INT_RAW The raw interrupt status of SYSTIMER_TARGET1_INT. (R/WTC/SS)
SYSTIMER_TARGET2_INT_RAW The raw interrupt status of SYSTIMER_TARGET2_INT. (R/WTC/SS)
```