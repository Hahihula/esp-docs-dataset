

```markdown
Chapter 10 System Timer (SYSTIMER)
Register 10.20. SYSTIMER_TARGET1_CONF_REG (0x0038)

SYSTIMER_TIMER_UNIT_SEL
SYSTIMER_TARGET1_PERIOD_MODE

(reserved)

| 31 | 30 | 29 | 26 | 25 | ... | 0 |
|-----|----|----|----|----|-----|---|
| 0   | 0  | 0  | 0  | 0  |     | Reset |
|     |     |     |     |     |     | 0x00000 |

SYSTIMER_TARGET1_PERIOD COMP1 alarm period. (R/W)
SYSTIMER_TARGET1_PERIOD_MODE Set COMP1 to period mode. (R/W)
SYSTIMER_TARGET1_TIMER_UNIT_SEL Select which unit to compare for COMP1. (R/W)

Register 10.21. SYSTIMER_COMP1_LOAD_REG (0x0054)

(reserved)

| 31 | ... | 1 | 0 |
|----|-----|---|---|
| 0  |     | Reset |

SYSTIMER_TIMER_COMP1_LOAD COMP1 synchronization enable signal. Set this bit to reload the alarm value/period to COMP1. (WT)

Register 10.22. SYSTIMER_TARGET2_HI_REG (0x002C)

(reserved)

| 31 | 20 | 19 | ... | 0 |
|----|----|----|-----|---|
| 0  |    |    |     | Reset |

SYSTIMER_TIMER_TARGET2_HI The alarm value to be loaded to COMP2, high 20 bits. (R/W)
```