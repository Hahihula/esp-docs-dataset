

```markdown
5. When the CPU is powered up, it begins unpacking the ROM and performing initialization. Then, recalculate the CRC code of the RTC fast memory. If it matches the result stored in LP_AON_STORE7_REG, the CPU will jump to the entry address of the RTC fast memory. Otherwise, the CPU will continue to run the boot code.

The boot flow after the chip's wake-up is shown in Figure 11.6-1.
```

![Figure 11.6-1. ESP32-H2 Boot Flow](image)

```markdown
## 11.7 Event Task Matrix Feature

The low-power management system on ESP32-H2 supports the Event Task Matrix (ETM) function, which allows the low-power management system's ETM tasks to be triggered by any peripherals' ETM events, or the low-power management system's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to the low-power management system. For more information, please refer to Chapter 10 Event Task Matrix (SOC_ETM).

The low-power management system can receive the following ETM tasks:

*   PMU_TASK_SLEEP_REQ: Triggers PMU's sleep process.
```

```markdown
Espressif Systems                          401                           ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```