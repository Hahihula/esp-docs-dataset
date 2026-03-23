
```markdown
14.4.4 Timer as Periodic Alarm by ETM

1. Enable the ETM module’s clock

2. Map ETM event to ETM task (which means using the event to trigger the task)

   - If TIMG_TO_AUTORELOAD is set to 1, map TIMERn_EVT_CNT_CMP_TIMERO (n:0-1) to the TIMERn_TASK_ALARM_START_TIMERO (n:0-1) by one ETM channel.

   - If TIMG_TO_AUTORELOAD is set to 0, in addition to mapping TIMERn_EVT_CNT_CMP_TIMERO (n:0-1) to the TIMERn_TASK_ALARM_START_TIMERO (n:0-1), the TIMERn_EVT_CNT_CMP_TIMERO (n:0-1) should also be mapped to TIMERn_TASK_CNT_RELOAD_TIMERO (n:0-1) by another ETM channel.

3. Choose to enable the one or two ETM channels.

4. Set TIMER_ETM_EN to 1 to enable timer group’s ETM events and tasks.

5. Configure the time-base counter following step 1 in Section 14.4.1.

6. Configure the alarm following step 2 in Section 14.4.2.

7. Configure the reload value via TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI.

8. Handle the TIMERn_EVT_CNT_CMP_TIMERO (n:0-1).

   - When alarm generates, the TIMERn_EVT_CNT_CMP_TIMERO (n:0-1) also generates, and the alarm generation will be disabled by the alarm.

   - If TIMG_TO_AUTORELOAD is 1, the current counter value is overwritten by the reloaded value. The alarm generation will be reopened by TIMERn_TASK_ALARM_START_TIMERO (n:0-1).

   - If TIMG_TO_AUTORELOAD is 0, the current counter value is overwritten by the reloaded value because of the TIMERn_TASK_CNT_RELOAD_TIMERO (n:0-1). The alarm generation will be reopened by TIMERn_TASK_ALARM_START_TIMERO (n:0-1).

9. Stop the timer (on final alarm iteration).

   - Disable the ETM channels used to map timer group’s event and task

   - Set TIMER_ETM_EN to 0.

   - Clear the interrupt by setting the timer’s corresponding bit in TIMG_TO_INT_CLR.

   - Disable the timer by clearing TIMG_TO_EN.
```

```markdown
14.4.5 RTC_SLOW_CLK Frequency Calculation

1. One-shot frequency calculation

   - Select the clock whose frequency is to be calculated (clock source of RTC_SLOW_CLK) via TIMG_RTC_CALI_CLK_SEL, and configure the time of calculation via TIMG_RTC_CALI_MAX.

   - Select one-shot frequency calculation by clearing TIMG_RTC_CALI_START_CYCLING, and enable the two counters via TIMG_RTC_CALI_START.

   - Once TIMG_RTC_CALI_RDY becomes 1, read TIMG_RTC_CALI_VALUE to get the value of XTAL_CLK’s counter, and calculate the frequency of RTC_SLOW_CLK according to the formula in Section 14.3.6.
```