

```markdown
Register 17.14. RTC_TIMER_LP_INT_RAW_REG (0x0038)

RTC_TIMER_MAIN_TIMER_LP_INT_RAW
RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_RAW

| 31 | 30 | 29 | ... | 0 |
|----:|----:|----:|-----|---|
|   0 |   0 |   0 | ... |   0 | Reset |

RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_RAW The raw interrupt status of RTC_TIMER_OVERFLOW_INT (LP CPU). (R/WTC/SS)

RTC_TIMER_MAIN_TIMER_LP_INT_RAW The raw interrupt status of RTC_TIMER_CMP1_INT. (R/WTC/SS)


Register 17.15. RTC_TIMER_LP_INT_ST_REG (0x003C)

RTC_TIMER_MAIN_TIMER_LP_INT_ST
RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_ST

| 31 | 30 | 29 | ... | 0 |
|----:|----:|----:|-----|---|
|   0 |   0 |   0 | ... |   0 | Reset |

RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_ST The masked interrupt status of RTC_TIMER_OVERFLOW_INT (LP CPU). (RO)

RTC_TIMER_MAIN_TIMER_LP_INT_ST The masked interrupt status of RTC_TIMER_CMP1_INT. (RO)
```