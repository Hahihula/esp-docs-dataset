

```markdown
Register 17.16. RTC_TIMER_LP_INT_ENA_REG (0x0040)

31    30    29
+------------------------------------------------------------------------------+
| RESERVED | RTC_TIMER_MAIN_TIMER_LP_INT_ENA | RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_ENA |
+------------------------------------------------------------------------------+

RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_ENA   Write 1 to enable RTC_TIMER_OVERFLOW_INT (LP CPU). (R/W)

RTC_TIMER_MAIN_TIMER_LP_INT_ENA           Write 1 to enable RTC_TIMER_CMP1_INT. (R/W)


Register 17.17. RTC_TIMER_LP_INT_CLR_REG (0x0044)

31    30    29
+------------------------------------------------------------------------------+
| RESERVED | RTC_TIMER_MAIN_TIMER_LP_INT_CLR | RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_CLR |
+------------------------------------------------------------------------------+

RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_CLR   Write 1 to clear RTC_TIMER_OVERFLOW_INT (LP CPU). (WT)

RTC_TIMER_MAIN_TIMER_LP_INT_CLR            Write 1 to clear RTC_TIMER_CMP1_INT. (WT)
```