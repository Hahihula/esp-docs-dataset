

```markdown
## 60.7 Registers

### 60.7.1 Interrupt and Status Registers

The addresses in this section are relative to Touch Sensor base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 60.1. RTC_TOUCH_INT_RAW_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| ... |             |
| 7   |             |
| 6   |             |
| 5   |             |
| 4   |             |
| 3   |             |
| 2   |             |
| 1   |             |
| 0   | Reset       |

RTC_TOUCH_SCAN_DONE_INT_RAW The raw interrupt status of TOUCH_SCAN_DONE_INT. (R/SS/WTC)

RTC_TOUCH_DONE_INT_RAW The raw interrupt status of TOUCH_DONE_INT. (R/SS/WTC)

RTC_TOUCH_ACTIVE_INT_RAW The raw interrupt status of TOUCH_ACTIVE_INT. (R/SS/WTC)

RTC_TOUCH_INACTIVE_INT_RAW The raw interrupt status of TOUCH_INACTIVE_INT. (R/SS/WTC)

RTC_TOUCH_TIMEOUT_INT_RAW The raw interrupt status of TOUCH_TIMEOUT_INT. (R/SS/WTC)

RTC_TOUCH_APPROACH_LOOP_DONE_INT_RAW The raw interrupt status of TOUCH_APPROACH_LOOP_DONE_INT. (R/SS/WTC)

RTC_TOUCH_BENCHMARK_UPDATE_INT_RAW The raw interrupt status of TOUCH_BENCHMARK_UPDATE_INT. (R/SS/WTC)
```