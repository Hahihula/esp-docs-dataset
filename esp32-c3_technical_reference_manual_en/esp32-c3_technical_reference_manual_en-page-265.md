

```markdown
|Bit|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
|Value|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|Reset|
```


Register 9.58. RTC_CNTL_INT_ENA_RTC_W1TC_REG (0x0104)

RTC_CNTL_SLP_WAKEUP_INT_ENA_W1TC Clear the interrupt enable bit when the chip wakes up from sleep by writing 1 to clear. (W1TC). (WO)

RTC_CNTL_SLP_REJECT_INT_ENA_W1TC Clear the interrupt enable bit when the chip rejects to go to sleep by writing 1 to clear (W1TC). (WO)

RTC_CNTL_WDT_INT_ENA_W1TC Clear the RTC watchdog interrupt enable bit by writing 1 to clear (W1TC). (WO)

RTC_CNTL_BROWN_OUT_INT_ENA_W1TC Clear the brownout interrupt enable bit by writing 1 to clear (W1TC). (WO)

RTC_CNTL_MAIN_TIMER_INT_ENA_W1TC Clear the RTC timer interrupt enable bit by writing 1 to clear. (W1TC). (WO)

RTC_CNTL_SWD_INT_ENA_W1TC Clear the super watchdog interrupt enable bit by writing 1 to clear (W1TC). (WO)

RTC_CNTL_XTAL32K_DEAD_INT_ENA_W1TC Clear the interrupt enable bit when the XTAL32K is dead by writing 1 to clear (W1TC). (WO)

RTC_CNTL_GLITCH_DET_INT_ENA_W1TC Clear the interrupt enable bit when a glitch is detected by writing 1 to clear (W1TC). (WO)

RTC_CNTL_BBPLL_CAL_INT_ENA_W1TC Clear the interrupt enable bit upon the ending of a bb_pll call by writing 1 to clear (W1TC).(WO)
```