

```markdown
Register 9.9. RTC_CNTL_TIMER2_REG (0x0020)

| 31 | 24 | 23 |        Field Description         |
|----|----|----|-----------------------------------|
|    |    | 0x1| RTC_CNTL_MIN_TIME_FOSC_OFF       |
|    | Reset|reserved|                               |

RTC_CNTL_MIN_TIME_FOSC_OFF Sets the minimal cycles for FOSC clock (using the RTC slow clock) when powered down. (R/W)

Register 9.10. RTC_CNTL_TIMER5_REG (0x002C)

| 31 | 16 | 15 |        Field Description         |
|----|----|----|-----------------------------------|
|    |reserved|RTC_CNTL_MIN_SLP_VAL|reserved|
|    |    |0x80|                               |

RTC_CNTL_MIN_SLP_VAL Sets the minimal sleep cycles (using the RTC slow clock). (R/W)
```