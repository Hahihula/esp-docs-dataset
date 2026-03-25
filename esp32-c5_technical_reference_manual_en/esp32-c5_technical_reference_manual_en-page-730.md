

```markdown
Register 17.5. RTC_TIMER_UPDATE_REG (0x0010)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            |                                                                             |
| 30  |                                            |                                                                             |
| 29  |                                            |                                                                             |
| 28  |                                            |                                                                             |
| 27  |                                            |                                                                             |
| 26  | RTC_TIMER_MAIN_TIMER_UPDATE               | Configures whether to log the current time through software configuration.   |
|     | (reserved)                                |                                                                             |
|     |                                            | O: Not log                                                                   |
|     |                                            | 1: Log                                                                       |
|     | (WT)                                      |                                                                             |
| 25  | RTC_TIMER_MAIN_TIMER_XTAL_OFF             | Configures whether to enable RTC Timer to log the time when the crystal powers up or down. |
|     |                                            | O: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |
| 24  | RTC_TIMER_MAIN_TIMER_SYS_STALL            | Configures whether to enable the RTC Timer to log the time when the CPU enters or exits the stall state. |
|     |                                            | O: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |
| 23  | RTC_TIMER_MAIN_TIMER_SYS_RST              | Configures whether to enable RTC Timer to log the time of system reset.       |
|     |                                            | O: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |

```
```plaintext
RTC_TIMER_MAIN_TIMER_UPDATE   Configures whether to log the current time through software configuration.
O: Not log
1: Log
(WT)

RTC_TIMER_MAIN_TIMER_XTAL_OFF   Configures whether to enable RTC Timer to log the time when the crystal powers up or down.
O: Disable
1: Enable
(R/W)

RTC_TIMER_MAIN_TIMER_SYS_STALL   Configures whether to enable the RTC Timer to log the time when the CPU enters or exits the stall state.
O: Disable
1: Enable
(R/W)

RTC_TIMER_MAIN_TIMER_SYS_RST   Configures whether to enable RTC Timer to log the time of system reset.
O: Disable
1: Enable
(R/W)
```