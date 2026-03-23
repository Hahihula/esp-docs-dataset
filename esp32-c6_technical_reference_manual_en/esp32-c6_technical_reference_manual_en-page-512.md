

```markdown
Chapter 13 System Timer (SYSTIMER)

Register 13.16. SYSTIMER_TARGETO_CONF_REG (0x0034)


| 31 | 30   | 29               | 26     | 25                  |
|----:|------:|------------------|--------|--------------------|
|    |       |                 |        |                    |
| SYSTIMER_TARGETO_TIMER_UNIT_SEL | reserved | SYSTIMER_TARGETO_PERIOD_MODE | SYSTIMER_TARGETO_PERIOD |

0x00000 Reset

SYSTIMER_TARGETO_PERIOD Configures COMPO alarm period. (R/W)

SYSTIMER_TARGETO_PERIOD_MODE Selects the two alarm modes for COMPO.
  0: Target mode
  1: Period mode
  (R/W)

SYSTIMER_TARGETO_TIMER_UNIT_SEL Chooses the counter value for comparison with COMPO.
  0: Use the count value from UNIT0
  1: Use the count value from UNIT1
  (R/W)


Register 13.17. SYSTIMER_COMPO_LOAD_REG (0x0050)

| 31 |      |
|----|------|
|    |  1   | 0 Reset

SYSTIMER_TIMER_COMPO_LOAD Configures whether or not to enable COMPO synchronization,
i.e., reload the alarm value/period to COMPO.
  0: No effect
  1: Enable COMPO synchronization
  (WT)
```