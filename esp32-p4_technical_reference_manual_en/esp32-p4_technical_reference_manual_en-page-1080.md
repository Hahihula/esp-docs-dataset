

```markdown
Chapter 15 System Timer

Register 15.24. SYSTIMER_TARGET2_CONF_REG (0x003C)

SYSTIMER_TARGET2_PERIOD Configures COMP2 alarm period. (R/W)
SYSTIMER_TARGET2_PERIOD_MODE Configures the two alarm modes for COMP2. See details in SYSTIMER_TARGETO_PERIOD_MODE. (R/W)
SYSTIMER_TARGET2_TIMER_UNIT_SEL Chooses the count value for comparison with COMP2. See details in SYSTIMER_TARGETO_TIMER_UNIT_SEL. (R/W)

Register 15.25. SYSTIMER_COMP2_LOAD_REG (0x0058)

SYSTIMER_TIMER_COMP2_LOAD Configures whether to enable COMP2 synchronization, i.e., reload the alarm value/period to COMP2.
0: No effect
1: Enable COMP2 synchronization
(WT)
```