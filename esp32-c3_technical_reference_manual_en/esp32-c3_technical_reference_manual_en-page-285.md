

```markdown
Register 10.23. SYSTIMER_TARGET2_LO_REG (0x0030)

SYSTIMER_TIMER_TARGET2_LO    The alarm value to be loaded to COMP2, low 32 bits. (R/W)


Register 10.24. SYSTIMER_TARGET2_CONF_REG (0x003C)

SYSTIMER_TARGET2_PERIOD      COMP2 alarm period. (R/W)
SYSTIMER_TARGET2_PERIOD_MODE Set COMP2 to period mode. (R/W)
SYSTIMER_TARGET2_TIMER_UNIT_SEL Select which unit to compare for COMP2. (R/W)


Register 10.25. SYSTIMER_COMP2_LOAD_REG (0x0058)

SYSTIMER_TIMER_COMP2_LOAD    COMP2 synchronization enable signal. Set this bit to reload the alarm value/period to COMP2. (WT)
```