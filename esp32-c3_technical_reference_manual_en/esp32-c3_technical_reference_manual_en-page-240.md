
```markdown
| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | RTC_CNTL_SLP_WAKEUP_INT_ENA               | Enables interrupts when chip wakes up from sleep. (R/W)                      |
| 29  | RTC_CNTL_SLP_REJECT_INT_ENA               | Enables interrupts when chip rejects to go to sleep. (R/W)                   |
| 28  | RTC_CNTL_WDT_INT_ENA                      | Enables the RTC watchdog interrupt. (R/W)                                   |
| 27  | RTC_CNTL_BROWN_OUT_INT_ENA                | Enables the brown-out interrupt. (R/W)                                      |
| 26  | RTC_CNTL_MAIN_TIMER_INT_ENA               | Enables the RTC timer interrupt. (R/W)                                      |
| 25  | RTC_CNTL_SWD_INT_ENA                      | Enables the super watchdog interrupt. (R/W)                                 |
| 24  | RTC_CNTL_XTAL32K_DEAD_INT_ENA             | Enables interrupts when the XTAL32K is dead. (R/W)                           |
| 23  | RTC_CNTL_GLITCH_DET_INT_ENA               | Enables interrupts when a glitch is detected. (R/W)                          |
| 22  | RTC_CNTL_BBPLL_CAL_INT_ENA                | Enables interrupts upon the ending of a bb_pll call. (R/W)                   |
| 21-0| (reserved)                                 |                                                                             |
```