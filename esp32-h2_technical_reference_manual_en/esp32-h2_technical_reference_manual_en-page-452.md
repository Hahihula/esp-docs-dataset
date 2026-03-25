

```markdown
Register 12.8. SYSTIMER_UNIT1_OP_REG (0x0008)

SYSTIMER_TIMER_UNIT1_VALUE_VALID Represents UNIT1 value is synchronized and valid.
(R/SS/WTC)

SYSTIMER_TIMER_UNIT1_UPDATE Configures whether or not to update timer UNIT1,
i.e., reads the UNIT1 count value to SYSTIMER_TIMER_UNIT1_VALUE_HI and SYS-
TIMER_TIMER_UNIT1_VALUE_LO.
O: No effect
1: Update timer UNIT1
(WT)

Register 12.9. SYSTIMER_UNIT1_LOAD_HI_REG (0x0014)

SYSTIMER_TIMER_UNIT1_LOAD_HI Configures the value to be loaded to UNIT1, high 20 bits. (R/W)
```