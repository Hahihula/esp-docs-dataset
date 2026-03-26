

```markdown
16.3.5 Event Task Matrix Feature

The TIMGn on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows TIMGn’s ETM tasks to be triggered by any peripherals’ ETM events, or TIMGn’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to TIMGn. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

TIMGn can receive the following ETM tasks:

- TGO_TASK_CNT_START_TIMERO: When triggered, it will enable the time-base counter.
- TG1_TASK_CNT_START_TIMERO: When triggered, it will enable the time-base counter.
- TGO_TASK_CNT_STOP_TIMERO: When triggered, it will disable the time-base counter.
- TG1_TASK_CNT_STOP_TIMERO: When triggered, it will disable the time-base counter.

Note:

The above two ETM tasks have the same function as the APB configuration TIMG_TO_EN. When these operations occur at the same time, the priority of each operation from high to low is as follows:

1. TGO_TASK_CNT_START_TIMERO and TG1_TASK_CNT_START_TIMERO: When triggered, it will enable the time-base counter;
2. TGO_TASK_CNT_STOP_TIMERO and TG1_TASK_CNT_STOP_TIMERO: When triggered, it will disable the time-base counter;
3. APB configuration TIMG_TO_EN: Enable or disable the time-base counter.

- TGO_TASK_ALARM_START_TIMERO: When triggered, it will enable the alarm generation.
- TG1_TASK_ALARM_START_TIMERO: When triggered, it will enable the alarm generation.

Note:

Alarm generation can also be enabled through APB method configuring TIMG_TO_ALARM_EN and hardware events. When these operations occur at the same time, the priority of each operation from high to low is as follows:

1. TGO_TASK_ALARM_START_TIMERO and TG1_TASK_ALARM_START_TIMERO: When triggered, it will enable the alarm generation;
2. Alarm events: When triggered, it will disable the alarm generation;
3. APB configuration TIMG_TO_ALARM_EN: Enable or disable the alarm generation.

- TGO_TASK_CNT_CAP_TIMERO: When triggered, it will update the current counter value to the TIMG_TOLO_REG and TIMG_TOHI_REG registers.
- TG1_TASK_CNT_CAP_TIMERO: When triggered, it will update the current counter value to the TIMG_TOLO_REG and TIMG_TOHI_REG registers.
- TGO_TASK_CNT_RELOAD_TIMERO: When triggered, it will overwrite the current counter value with the reload value stored in TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI.
- TG1_TASK_CNT_RELOAD_TIMERO: When triggered, it will overwrite the current counter value with the
```