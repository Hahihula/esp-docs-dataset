

```markdown
- Register group 1 includes register `RTC_TIMER_MAIN_BUF1_LOW_REG` and `RTC_TIMER_MAIN_BUF1_HIGH_REG`, which are used to cache the count value of the RTC Timer from the last trigger.
- On a new trigger, the record from the previous trigger will be moved from register group 0 to register group 1 (and the previous record in register group 1 will be overwritten), and the record of this trigger will be stored in register group 0. Therefore, only the last two triggers can be logged at any time.

## 18.4 Event Task Matrix Feature

The RTC Timer on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows RTC Timer’s ETM tasks to be triggered by any peripherals’ ETM events, or RTC Timer’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to RTC Timer. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

RTC Timer doesn't receive any ETM tasks:

RTC Timer can generate the following ETM events:
* `RTC_EVT_CMP`: Indicate that the RTC Timer reaches the target time 0 configured by `RTC_TIMER_MAIN_TIMER_TAR_LOW0` and `RTC_TIMER_MAIN_TIMER_TAR_HIGH0`.
* `RTC_EVT_OVF`: Indicate the 48-bit counter overflow.
* `RTC_EVT_TICK`: Indicates the event that occurs when the RTC timer increments by 1.

## 18.5 Interrupts

ESP32-P4’s RTC Timer can generate the following interrupt signal(s) that will be sent to the **Interrupt Matrix**:
* `LP_TIMER_REG_O_INTR`
* `LP_TIMER_REG_1_INTR`

There are several internal interrupt sources from RTC Timer that can generate the above interrupt signal(s). The interrupt sources from RTC Timer are listed with their trigger conditions and the resulted interrupt signal(s) in Table 18.5-1.

Table 18.5-1. RTC Timer’s Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                     | Interrupt Signal                  |
|---------------------------|----------------------------------------|------------------------------------|
| `RTC_TIMER_CMPO_INT`      | RTC Timer reaches the target time 0   | `LP_TIMER_REG_O_INTR`             |
| `RTC_TIMER_CMP1_INT`      | RTC Timer reaches the target time 1   | `LP_TIMER_REG_1_INTR`             |
| `RTC_TIMER_OVERFLOW_INT`  | 48-bit counter overflow               | `LP_TIMER_REG_O_INTR`, `LP_TIMER_REG_1_INTR` |

**Note:**
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```