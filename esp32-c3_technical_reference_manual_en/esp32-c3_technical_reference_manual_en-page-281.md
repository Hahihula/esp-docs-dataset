

```markdown
Register 10.11. SYSTIMER_UNIT1_VALUE_HI_REG (0x0048)
```

| Bit Range | Description         |
|-----------|---------------------|
| 31        | reserved            |
| 20..19    |                     |
| 0         | Reset               |

SYSTIMER_TIMER_UNIT1_VALUE_HI UNIT1 read value, high 20 bits. (RO)

```
Register 10.12. SYSTIMER_UNIT1_VALUE_LO_REG (0x004C)
```

| Bit Range | Description         |
|-----------|---------------------|
| 31        |                     |
|           |                     |
|           | Reset               |

SYSTIMER_TIMER_UNIT1_VALUE_LO UNIT1 read value, low 32 bits. (RO)

```
Register 10.13. SYSTIMER_UNIT1_LOAD_REG (0x0060)
```

| Bit Range | Description         |
|-----------|---------------------|
| 31        |                     |
|           |                     |
|           | Reset               |

SYSTIMER_TIMER_UNIT1_LOAD UNIT1 synchronization enable signal. Set this bit to reload the values of SYSTIMER_TIMER_UNIT1_LOAD_HI and SYSTIMER_TIMER_UNIT1_LOAD_LO to UNIT1. (WT)
```