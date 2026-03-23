

```markdown
Chapter 12 Low-Power Management

GoBack

Figure 12.6-1. ESP32-C6 Boot Flow

12.7 Event Task Matrix Feature

The low-power management system on ESP32-C6 supports the Event Task Matrix (ETM) function, which allows the low-power management system's ETM tasks to be triggered by any peripherals' ETM events, or the low-power management system's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to the low-power management system. For more information, please refer to Chapter 11 Event Task Matrix (SOC_ETM).

The low-power management system can receive the following ETM tasks:

- PMU_TASK_SLEEP_REQ: Triggers PMU's sleep process.

The low-power management system can generate the following ETM events:

- PMU_EVT_SLEEP_WAKEUP: Indicates that PMU is woken up to the HP_ACTIVE state.
- RTC_EVT_TICK: Indicates that the RTC timer increments by 1.
```