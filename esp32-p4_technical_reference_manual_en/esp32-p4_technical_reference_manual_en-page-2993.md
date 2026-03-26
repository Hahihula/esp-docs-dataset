

```markdown
Register 60.4. RTC_TOUCH_INT_CLR_REG (0x000C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30-7| reserved                                    |                                                                             |
| 6   | RTC_TOUCH_BENCHMARK_UPDATE_INT_CLR         | Write 1 to clear TOUCH_BENCHMARK_UPDATE_INT. (WT)                           |
| 5   | RTC_TOUCH_APPROACH_LOOP_DONE_INT_CLR       | Write 1 to clear TOUCH_APPROACH_LOOP_DONE_INT. (WT)                         |
| 4   | RTC_TOUCH_TIMEOUT_INT_CLR                  | Write 1 to clear TOUCH_TIMEOUT_INT. (WT)                                   |
| 3   | RTC_TOUCH_INACTIVE_INT_CLR                 | Write 1 to clear TOUCH_INACTIVE_INT. (WT)                                  |
| 2   | RTC_TOUCH_ACTIVE_INT_CLR                   | Write 1 to clear TOUCH_ACTIVE_INT. (WT)                                    |
| 1   | RTC_TOUCH_DONE_INT_CLR                     | Write 1 to clear TOUCH_DONE_INT. (WT)                                      |
| 0   | RTC_TOUCH_SCAN_DONE_INT_CLR                | Write 1 to clear TOUCH_DONE_INT. (WT)                                      |

```
```markdown
RTC_TOUCH_SCAN_DONE_INT_CLR    Write 1 to clear TOUCH_DONE_INT. (WT)

RTC_TOUCH_DONE_INT_CLR         Write 1 to clear TOUCH_DONE_INT. (WT1)

RTC_TOUCH_ACTIVE_INT_CLR       Write 1 to clear TOUCH_ACTIVE_INT. (WT)

RTC_TOUCH_INACTIVE_INT_CLR     Write 1 to clear TOUCH_INACTIVE_INT. (WT)

RTC_TOUCH_TIMEOUT_INT_CLR      Write 1 to clear TOUCH_TIMEOUT_INT. (WT)

RTC_TOUCH_APPROACH_LOOP_DONE_INT_CLR Write 1 to clear TOUCH_APPROACH_LOOP_DONE_INT. (WT)

RTC_TOUCH_BENCHMARK_UPDATE_INT_CLR Write 1 to clear TOUCH_BENCHMARK_UPDATE_INT.
```