

```markdown
Note:

The above two ETM tasks have the same function as the APB configuration TIMGn_TO_EN. When these operations occur at the same time, the priority of each operation from high to low is as follows:
1. TIMERn_TASK_CNT_START_TIMERO: When triggered, it will enable the time-base counter;
2. TIMERn_TASK_CNT_STOP_TIMERO: When triggered, it will disable the time-base counter;
3. APB configuration TIMGn_TO_EN: When triggered, it will enable or disable the time-base counter.

• TIMERn_TASK_ALARM_START_TIMERO (n:0-1): When triggered, it will enable the alarm generation.

Note:

Alarm generation can also be enabled through APB method configuring TIMGn_ALARM_EN and hardware events. When these operations occur at the same time, the priority of each operation from high to low is as follows:
1. TIMERn_TASK_ALARM_START_TIMERO: When triggered, it will enable the alarm generation;
2. Alarm events: When triggered, it will disable the alarm generation;
3. APB configuration TIMGn_TO_ALARM_EN: When triggered, it will enable or disable the alarm generation.

• TIMERn_TASK_CNT_CAP_TIMERO (n:0-1): When triggered, it will update the current counter value to the TIMGn_TOLO_REG and TIMGn_TOHI_REG registers.
• TIMERn_TASK_CNT_RELOAD_TIMERO (n:0-1): When triggered, it will overwrite the current counter value with the reload value stored in TIMGn_TO_LOAD_LO and TIMGn_TO_LOAD_HI.

The timer groups can generate the following ETM events:
• TIMERn_EVT_CNT_CMP_TIMERO (n:0-1): Indicates the interrupt event of TO in TIMGn.

All the ETM tasks and events will not take effect until the TIMGn_ETM_EN is set to 1.
In practical applications, timer groups’ ETM events can trigger their own ETM tasks. For example, TIMERn_TASK_ALARM_START_TIMERO (n:0-1) can be triggered by TIMERn_EVT_CNT_CMP_TIMERO (n:0-1) to realize periodic alarm. For configuration steps, please refer to 13.4.4 Timer as Periodic Alarm by ETM.

13.3.6 RTC_SLOW_CLK Frequency Calculation

Using XTAL_CLK as a reference, it is possible to calculate the frequency of clock sources for RTC_SLOW_CLK (i.e., RTC_SLOW_CLK, RC_FAST_DIV_CLK, and XTAL32K_CLK) as follows. However, please note only TIMG0 supports this function.

1. Start periodic or one-shot frequency calculation (see Section 13.4.5 for details);
2. Once receiving the signal to start the calculation, the counter of XTAL_CLK and the counter of RTC_SLOW_CLK begin to work at the same time. When the counter of RTC_SLOW_CLK counts to C0, the two counters stop counting simultaneously;
3. Assume the value of XTAL_CLK’s counter is C1, and the frequency of RTC_SLOW_CLK would be calculated as: f_rtc = (C0 × f_XTAL_CLK) / C1
```