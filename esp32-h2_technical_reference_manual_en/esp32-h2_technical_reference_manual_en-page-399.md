

```markdown
| Triggering Conditions                     | Description                                                                                                                                 |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| RTC_TIMER_MAIN_TIMER_XTAL_OFF            | Triggered when PMU powers up or down the 40 MHz crystal.                                                                                      |
| RTC_TIMER_MAIN_TIMER_SYS_STALL           | Triggered when the CPU enters or exits the stall state. This is to ensure the system timer is continuous in time.                              |
| RTC_TIMER_MAIN_TIMER_SYS_RST             | Triggered upon system reset.                                                                                                                  |
| RTC_TIMER_UPDATE                          | Triggered when RTC_TIMER_UPDATE is configured by the CPU (e.g., users).                                                                      |

The RTC timer updates two groups of registers upon any new trigger.

- Register group 0 records the count value of the RTC timer under the current trigger, with the counting unit being LP_SLOW_CLK.
    - RTC_TIMER_MAIN_BUF0_HIGH
    - RTC_TIMER_MAIN_BUF0_LOW

- Register group 1 records the count value of the RTC timer under the previous trigger.
    - RTC_TIMER_MAIN_BUF1_HIGH
    - RTC_TIMER_MAIN_BUF1_LOW

Whenever a new trigger occurs, the following process takes place:
1. The record from the previous trigger is moved from register group 0 to register group 1.
2. The record in register group 1 will be overwritten.
3. The record of the current trigger is then stored in register group 0.
```