

```markdown
Register 12.10. SYSTIMER_UNIT1_LOAD_LO_REG (0x0018)

SYSTIMER_TIMER_UNIT1_LOAD_LO

31 | 0 | Reset
---|----|------
   |    |

SYSTIMER_TIMER_UNIT1_LOAD_LO Configures the value to be loaded to UNIT1, low 32 bits. (R/W)

Register 12.11. SYSTIMER_UNIT1_VALUE_HI_REG (0x0048)

SYSTIMER_TIMER_UNIT1_VALUE_HI

31 | 20 | 19 | 0
---|-----|----|----
reserved |    |     |
   |      |      |

SYSTIMER_TIMER_UNIT1_VALUE_HI Represents UNIT1 read value, high 20 bits. (RO)

Register 12.12. SYSTIMER_UNIT1_VALUE_LO_REG (0x004C)

SYSTIMER_TIMER_UNIT1_VALUE_LO

31 | 0 | Reset
---|----|------
   |    |

SYSTIMER_TIMER_UNIT1_VALUE_LO Represents UNIT1 read value, low 32 bits. (RO)
```