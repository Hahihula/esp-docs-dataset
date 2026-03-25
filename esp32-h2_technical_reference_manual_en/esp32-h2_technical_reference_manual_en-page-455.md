

```markdown
Chapter 12 System Timer (SYSTIMER)

Register 12.16. SYSTIMER_TARGETO_CONF_REG (0x0034)

| Bit | Description |
|-----|-------------|
| 31  | SYS TIMER TARGET O TIMER UNIT SEL |
| 30  | SYS TIMER TARGET O PERIOD MODE   |
|     | (reserved)                      |
| 29  |                                     |
| 28  |                                     |
| 27  |                                     |
| 26  |                                     |
| 25  |                                     |
| ... |                                     |
| 0   |                                     |

Reset: 0x00000

SYSTIMER_TARGETO_TO_PERIOD Configures the alarm period to be loaded to COMPO. (R/W)

SYSTIMER_TARGETO_TO_PERIOD_MODE Selects an alarm mode for COMPO.
    0: Target mode
    1: Period mode
    (R/W)

SYSTIMER_TARGETO_TO_TIMER_UNIT_SEL Configures the counter value for comparison with COMPO.
    0: Use the count value from UNIT0
    1: Use the count value from UNIT1
    (R/W)

Register 12.17. SYSTIMER_COMPO_LOAD_REG (0x0050)

| Bit | Description |
|-----|-------------|
| 31  | SYS TIMER TIMER COMPO LOAD      |
| ... |                                     |
| 0   |                                     |

Reset: 0

SYSTIMER_TIMER_COMPO_LOAD Configures whether or not to enable COMPO synchronization,
i.e., reload the alarm value/period to COMPO.
    0: No effect
    1: Enable COMPO synchronization
    (WT)
```