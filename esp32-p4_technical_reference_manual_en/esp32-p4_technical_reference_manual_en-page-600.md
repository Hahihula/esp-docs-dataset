

```markdown
Register 9.39. GPIO_INT_RAW_REG (0x0700)

| Bit 31 | ... | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|---|---|
|        |     |   |   |   |   |   |   | Reset |

GPIO_COMPO_NEG_INT_RAW    The raw interrupt status of GPIO_COMPO_NEG_INT. (R/WTC/SS)
GPIO_COMPO_POS_INT_RAW    The raw interrupt status of GPIO_COMPO_POS_INT. (R/WTC/SS)
GPIO_COMPO_ALL_INT_RAW    The raw interrupt status of GPIO_COMPO_ALL_INT. (R/WTC/SS)

GPIO_COMP1_NEG_INT_RAW    The raw interrupt status of GPIO_COMP1_NEG_INT. (R/WTC/SS)
GPIO_COMP1_POS_INT_RAW    The raw interrupt status of GPIO_COMP1_POS_INT. (R/WTC/SS)
GPIO_COMP1_ALL_INT_RAW    The raw interrupt status of GPIO_COMP1_ALL_INT. (R/WTC/SS)

Register 9.40. GPIO_INT_ST_REG (0x0704)

| Bit 31 | ... | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|---|---|
|        |     |   |   |   |   |   |   | Reset |

GPIO_COMPO_NEG_INT_ST    The masked interrupt status of GPIO_COMPO_NEG_INT. (RO)
GPIO_COMPO_POS_INT_ST    The masked interrupt status of GPIO_COMPO_POS_INT. (RO)
GPIO_COMPO_ALL_INT_ST    The masked interrupt status of GPIO_COMPO_ALL_INT. (RO)

GPIO_COMP1_NEG_INT_ST    The masked interrupt status of GPIO_COMP1_NEG_INT. (RO)
GPIO_COMP1_POS_INT_ST    The masked interrupt status of GPIO_COMP1_POS_INT. (RO)
GPIO_COMP1_ALL_INT_ST    The masked interrupt status of GPIO_COMP1_ALL_INT. (RO)
```