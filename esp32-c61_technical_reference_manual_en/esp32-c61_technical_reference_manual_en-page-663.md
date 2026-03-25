

```markdown
Register 15.3. RTC_TIMER_UPDATE_REG (0x0010)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | RTC_TIMER_MAIN_TIMER_SYS_RST                                               |
| 30  | RTC_TIMER_MAIN_TIMER_SYS_STALL                                             |
| 29  | RTC_TIMER_MAIN_TIMER_XTAL_OFF                                             |
| 28  | RTC_TIMER_MAIN_TIMER_UPDATE                                               |
| 27  | (reserved)                                                                 |
| 26  | (reserved)                                                                 |
| ... | ...                                                                        |
| 0   | Reset                                                                      |

RTC_TIMER_MAIN_TIMER_UPDATE Configures whether to log the current time through software configuration.
O: Not log
1: Log
(WT)

RTC_TIMER_MAIN_TIMER_XTAL_OFF Configures whether to enable RTC Timer to log the time when the crystal powers up or down.
O: Disable
1: Enable
(R/W)

RTC_TIMER_MAIN_TIMER_SYS_STALL Configures whether to enable the RTC Timer to log the time when the CPU enters or exits the stall state.
O: Disable
1: Enable
(R/W)

RTC_TIMER_MAIN_TIMER_SYS_RST Configures whether to enable RTC Timer to log the time of system reset.
O: Disable
1: Enable
(R/W)
```