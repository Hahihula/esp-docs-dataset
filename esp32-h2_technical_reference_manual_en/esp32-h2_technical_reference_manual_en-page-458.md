

```markdown
Chapter 12 System Timer (SYSTIMER)

Register 12.24. SYSTIMER_TARGET2_CONF_REG (0x003C)

SYSTIMER_TARGET2_TIMER_UNIT_SEL
SYSTIMER_TARGET2_PERIOD_MODE

(reserved)

| 31 | 30 | 29 | 26 | 25 |
|-----|----|----|----|----|
| 0   | 0  | 0  | 0  | 0  |

0x00000 Reset

SYSTIMER_TARGET2_PERIOD Configures COMP2 alarm period. (R/W)

SYSTIMER_TARGET2_PERIOD_MODE Selects an alarm mode for COMP2. See details in SYS-TIMER_TARGETO_TO_PERIOD_MODE. (R/W)

SYSTIMER_TARGET2_TIMER_UNIT_SEL Chooses the counter value for comparison with COMP2.
See details in SYSTIMER_TARGETO_TO_TIMER_UNIT_SEL. (R/W)

Register 12.25. SYSTIMER_COMP2_LOAD_REG (0x0058)

(reserved)

| 31 |
|----|
| 0  | 1 |

SYSTIMER_TIMER_COMP2_LOAD Configures whether or not to enable COMP2 synchronization,
i.e., reload the alarm value/period to COMP2.

0: No effect

1: Enable COMP2 synchronization
(WT)
```