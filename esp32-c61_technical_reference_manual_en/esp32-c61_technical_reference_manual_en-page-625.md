

```markdown
13.4.5 Frequency Calculation of Slow Clock for Timer Group O

Using XTAL_CLK as a reference, it is possible to calculate the frequency of slow clock sources provided by ESP32-C61. For the slow clock inputted to the timer group, please refer to 9 Interrupt Matrix > 9.2 Interrupt Terminology in ESP32-C61. The calculation method is as follows:

1. Start periodic or one-shot frequency calculation (see Section 13.7.5 for details);
2. Once receiving the signal to start calculation, the counter of XTAL_CLK and the counter of slow clock begin to work at the same time. When the counter of slow clock counts to C0, the two counters stop counting simultaneously;
3. Assume the value of XTAL_CLK's counter is C1, and the frequency of slow clock would be calculated as:

    f_rtc = (C0 × f_XTAL_CLK) / C1

Please note that the input frequency should not be larger than f_XTAL_CLK / 2 when calculating the frequency of slow clock.

13.5 Event Task Matrix Feature

The timer groups on ESP32-C61 support the Event Task Matrix (ETM) function, which allows timer groups' ETM tasks to be triggered by any peripherals' ETM events, or timer groups' ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to timer groups. For more information, please refer to Chapter 10 Event Task Matrix (ETM).

The timer groups can receive the following ETM tasks:

- TGO_TASK_CNT_START_TIMERO: When triggered, it will enable the time-base counter.
- TG1_TASK_CNT_START_TIMERO: When triggered, it will enable the time-base counter.
- TGO_TASK_CNT_STOP_TIMERO: When triggered, it will disable the time-base counter.
- TG1_TASK_CNT_STOP_TIMERO: When triggered, it will disable the time-base counter.

Note:

The above two ETM tasks have the same function as the APB configuration TIMG_TO_EN. When these operations occur at the same time, the priority of each operation from high to low is as follows:

1. TGO_TASK_CNT_START_TIMERO and TG1_TASK_CNT_START_TIMERO: When triggered, it will enable the time-base counter;
2. TGO_TASK_CNT_STOP_TIMERO and TG1_TASK_CNT_STOP_TIMERO: When triggered, it will disable the time-base counter;
3. APB configuration TIMG_TO_EN: When triggered, it will enable or disable the time-base counter.

- TGO_TASK_ALARM_START_TIMERO: When triggered, it will enable the alarm generation.
- TG1_TASK_ALARM_START_TIMERO: When triggered, it will enable the alarm generation.

Note:

Alarm generation can also be configured through APB method and hardware events. When these operations
```