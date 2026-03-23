

```markdown
|Bit|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|:----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|Reset|

```
RTC_CNTL_SLP_WAKEUP_INT_ST Stores the status of the interrupt triggered when the chip wakes up from sleep. (RO)

RTC_CNTL_SLP_REJECT_INT_ST Stores the status of the interrupt triggered when the chip rejects to go to sleep. (RO)

RTC_CNTL_WDT_INT_ST Stores the status of the RTC watchdog interrupt. (RO)

RTC_CNTL_BROWN_OUT_INT_ST Stores the status of the brownout interrupt. (RO)

RTC_CNTL_MAIN_TIMER_INT_ST Stores the status of the RTC main timer interrupt. (RO)

RTC_CNTL_SWD_INT_ST Stores the status of the super watchdog interrupt. (RO)

RTC_CNTL_XTAL32K_DEAD_INT_ST Stores the status of the interrupt triggered when the XTAL32K is dead. (RO)

RTC_CNTL_GLITCH_DET_INT_ST Stores the status of the interrupt triggered when a glitch is detected. (RO)

RTC_CNTL_BBPLL_CAL_INT_ST Stores the status of the interrupt triggered upon the ending of a bbpll call. (RO)
```