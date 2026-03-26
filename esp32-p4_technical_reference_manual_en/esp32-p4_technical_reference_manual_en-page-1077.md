

```markdown
Chapter 15 System Timer

Register 15.16. SYSTIMER_TARGETO_CONF_REG (0x0034)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | SYSTIMER_TARGETO_TIMER_UNIT_SEL |
| 30  | SYSTIMER_TARGETO_PERIOD_MODE    |
|     | (reserved)                      |
| 26  |                                 |
| 25  |                                 |
| 0   | 0 0 0 0                         |
|     | 0x00000                         |
|     | Reset                           |

SYSTIMER_TARGETO_TO_PERIOD Configures COMPO alarm period. (R/W)

SYSTIMER_TARGETO_TO_PERIOD_MODE Selects the two alarm modes for COMPO.
0: Target mode
1: Period mode
(R/W)

SYSTIMER_TARGETO_TO_TIMER_UNIT_SEL Chooses the count value for comparison with COMPO.
0: Use the count value from UNIT0
1: Use the count value from UNIT1
(R/W)

Register 15.17. SYSTIMER_COMPO_LOAD_REG (0x0050)

| Bit | Description                     |
|-----|---------------------------------|
| 31  |                                 |
|     | (reserved)                      |
| 1   |                                 |
| 0   | 0 0 0 0                         |
|     | Reset                           |

SYSTIMER_TIMER_COMPO_LOAD Configures whether to enable COMPO synchronization, i.e.,
reload the alarm value/period to COMPO.
0: No effect
1: Enable COMPO synchronization
(WT)
```