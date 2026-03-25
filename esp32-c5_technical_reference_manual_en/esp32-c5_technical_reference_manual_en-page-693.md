

```markdown
3. Enable auto reload by setting TIMG_TO_AUTORELOAD and configure the reload value via TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI.
4. Start the alarm by setting TIMG_TO_ALARM_EN.
5. Handle the alarm interrupt (repeat on each alarm iteration).
  - Clear the interrupt by setting the timer’s corresponding bit in TIMG_TO_INT_CLR.
  - If the next alarm requires a new alarm value and reload value (i.e., different alarm interval per iteration), then TIMG_TOALARMLO_REG, TIMG_TOALARMI_REG, TIMG_TO_LOAD_LO, and TIMG_TO_LOAD_HI should be reconfigured as needed. Otherwise, the aforementioned registers should remain unchanged.
    - Re-enable the alarm by setting TIMG_TO_ALARM_EN.
6. Stop the timer (on final alarm iteration).
  - Clear the interrupt by setting the timer’s corresponding bit in TIMG_TO_INT_CLR.
  - Disable the timer by clearing TIMG_TO_EN.

15.7.4 Timer as Periodic Alarm by ETM

1. Enable the ETM module’s clock
2. Map ETM event to ETM task (which means using the event to trigger the task)
  - If TIMG_TO_AUTORELOAD is set to 1, map TGO_EVT_CNT_CMP_TIMERO and TG1_EVT_CNT_CMP_TIMERO to the TGO_TASK_ALARM_START_TIMERO and TG1_TASK_ALARM_START_TIMERO respectively by one ETM channel.
  - If TIMG_TO_AUTORELOAD is set to 0, in addition to mapping TGO_EVT_CNT_CMP_TIMERO and TG1_EVT_CNT_CMP_TIMERO to the TGO_TASK_ALARM_START_TIMERO and TG1_TASK_ALARM_START_TIMERO, the TGO_EVT_CNT_CMP_TIMERO and TG1_EVT_CNT_CMP_TIMERO should also be mapped to TGO_TASK_CNT_RELOAD_TIMERO and TG1_TASK_CNT_RELOAD_TIMERO by another ETM channel.
3. Choose to enable the one or two ETM channels.
4. Set TIMER_ETM_EN to 1 to enable timer group’s ETM events and tasks.
5. Configure the time-base counter following step 1 in Section 15.7.1.
6. Configure the alarm following step 2 in Section 15.7.2.
7. Configure the reload value via TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI.
8. Handle the TGO_EVT_CNT_CMP_TIMERO and TG1_EVT_CNT_CMP_TIMERO.
  - When alarm generates, the TGO_EVT_CNT_CMP_TIMERO and TG1_EVT_CNT_CMP_TIMERO also generate, and the alarm generation will be disabled by the alarm.
  - If TIMG_TO_AUTORELOAD is 1, the current counter value is overwritten by the reloaded value. The alarm generation will be reopened by TGO_TASK_ALARM_START_TIMERO and TG1_TASK_ALARM_START_TIMERO.
```