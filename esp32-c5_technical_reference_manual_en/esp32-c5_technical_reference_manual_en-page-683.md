

```markdown
## Register 14.28. SYSTIMER_INT_CLR_REG (0x006C)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   |   | Reset |

SYSTIMER_TARGETO_INT_CLR Write 1 to clear SYSTIMER_TARGETO_INT. (WT)
SYSTIMER_TARGET1_INT_CLR Write 1 to clear SYSTIMER_TARGET1_INT. (WT)
SYSTIMER_TARGET2_INT_CLR Write 1 to clear SYSTIMER_TARGET2_INT. (WT)

## Register 14.29. SYSTIMER_INT_ST_REG (0x0070)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   |   | Reset |

SYSTIMER_TARGETO_INT_ST The masked interrupt status of SYSTIMER_TARGETO_INT. (RO)
SYSTIMER_TARGET1_INT_ST The masked interrupt status of SYSTIMER_TARGET1_INT. (RO)
SYSTIMER_TARGET2_INT_ST The masked interrupt status of SYSTIMER_TARGET2_INT. (RO)

## Register 14.30. SYSTIMER_REAL_TARGETO_LO_REG (0x0074)

| Bit 31 | ... |
|--------|-----|
|        |     |

SYSTIMER_TARGETO_LO_RO Represents the actual target value of COMPO, low 32 bits. (RO)
```