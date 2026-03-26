

```markdown
Chapter 15 System Timer

Register 15.21. SYSTIMER_COMP1_LOAD_REG (0x0054)

SYSTIMER_TIMER_COMP1_LOAD Configures whether to enable COMP1 synchronization, i.e., reload the alarm value/period to COMP1.
O: No effect
1: Enable COMP1 synchronization
(WT)

Register 15.22. SYSTIMER_TARGET2_HI_REG (0x002C)

SYSTIMER_TIMER_TARGET2_HI Configures the alarm value to be loaded to COMP2, high 20 bits.
(R/W)

Register 15.23. SYSTIMER_TARGET2_LO_REG (0x0030)

SYSTIMER_TIMER_TARGET2_LO Configures the alarm value to be loaded to COMP2, low 32 bits.
(R/W)
```