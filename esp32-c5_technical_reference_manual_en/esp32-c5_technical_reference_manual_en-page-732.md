

```markdown
Register 17.9. RTC_TIMER_MAIN_BUF1_HIGH_REG (0x0020)

31                                 16                 15                  0
+--------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 |                                0                               | Reset |
+--------------------------------------------------------------------------------------------------+

RTC_TIMER_MAIN_TIMER_BUF1_HIGH Represents the high 16 bits of the cached value 1 in RTC Timer. (RO)

Register 17.10. RTC_TIMER_INT_RAW_REG (0x0028)

31   30                         29                  0
+---------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 |                                0                               | Reset |
+---------------------------------------------------------------------------------------------+

RTC_TIMER_OVERFLOW_RAW The raw interrupt status of RTC_TIMER_OVERFLOW_INT (HP CPU). (R/WTC/SS)

RTC_TIMER_SOC_WAKEUP_INT_RAW The raw interrupt status of RTC_TIMER_CMPO_INT. (R/WTC/SS)
```