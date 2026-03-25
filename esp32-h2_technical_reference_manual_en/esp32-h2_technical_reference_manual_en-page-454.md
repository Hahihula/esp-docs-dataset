

```markdown
Chapter 12 System Timer (SYSTIMER) GoBack


Register 12.13. SYSTIMER_UNIT1_LOAD_REG (0x0060)

```
| 31 | 0 |
|----:|---|
| (reserved) | SYSTIMER_TIMER_UNIT1_LOAD |
| Reset |

SYSTIMER_TIMER_UNIT1_LOAD Configures whether or not to reload the value of UNIT1, i.e., reload the values of `SYSTIMER_TIMER_UNIT1_VALUE_HI` and `SYSTIMER_TIMER_UNIT1_VALUE_LO` to UNIT1.
0: No effect
1: Reload the value of UNIT1
(WT)


Register 12.14. SYSTIMER_TARGETO_HI_REG (0x001C)

```
| 31 | 20 | 19 |
|----:|----:|---|
| (reserved) | SYSTIMER_TIMER_TARGETO_HI | Reset |

SYSTIMER_TIMER_TARGETO_HI Configures the alarm value to be loaded to COMPO, high 20 bits.
(R/W)


Register 12.15. SYSTIMER_TARGETO_LO_REG (0x0020)

```
| 31 |
|----:|
| SYSTIMER_TIMER_TARGETO_LO | Reset |

SYSTIMER_TIMER_TARGETO_LO Configures the alarm value to be loaded to COMPO, low 32 bits.
(R/W)
```