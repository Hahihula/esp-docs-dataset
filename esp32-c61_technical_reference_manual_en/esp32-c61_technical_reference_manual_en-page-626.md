

```markdown
occur at the same time, the priority of each operation from high to low is as follows:

1. TGO_TASK_ALARM_START_TIMERO and TG1_TASK_ALARM_START_TIMERO: When triggered, it will enable the alarm generation;
2. Alarm events: When triggered, it will disable the alarm generation;
3. APB configuration TIMG_ALARM_EN: When triggered, it will enable or disable the alarm generation.

* TGO_TASK_CNT_CAP_TIMERO: When triggered, it will update the current counter value to the TIMG_TOLO_REG and TIMG_TOHI_REG registers.
* TG1_TASK_CNT_CAP_TIMERO: When triggered, it will update the current counter value to the TIMG_TOLO_REG and TIMG_TOHI_REG registers.
* TGO_TASK_CNT_RELOAD_TIMERO: When triggered, it will overwrite the current counter value with the reload value stored in TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI.
* TG1_TASK_CNT_RELOAD_TIMERO: When triggered, it will overwrite the current counter value with the reload value stored in TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI.

The timer groups can generate the following ETM events:

* TGO_EVT_CNT_CMP_TIMERO: Indicates the interrupt event of TO in TIMGO.
* TG1_EVT_CNT_CMP_TIMERO: Indicates the interrupt event of TO in TIMG1.

All the ETM tasks and events will not take effect until the TIMG_ETM_EN is set to 1.

In practical applications, timer groups’ ETM events can trigger their own ETM tasks. For example, TGO_TASK_ALARM_START_TIMERO and TG1_TASK_ALARM_START_TIMERO can be triggered respectively by TGO_EVT_CNT_CMP_TIMERO and TG1_EVT_CNT_CMP_TIMERO to realize periodic alarm. For configuration steps, please refer to 13.7.4 Timer as Periodic Alarm by ETM.

## 13.6 Interrupts

ESP32-C61’s TIMGn can generate the following interrupt signal(s) that will be sent to the Interrupt Matrix.

* TGn_TO_INTR
* TGn_WDT_INTR

There are several internal interrupt sources from TIMGn that can generate the above interrupt signals. The interrupt sources from TIMGn are listed with their trigger conditions and the resulted interrupt signals in Table 13.6-1.

Table 13.6-1. TIMGn’s Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                     | Interrupt Signal   |
|----------------------------|----------------------------------------|--------------------|
| TIMG_TO_INT                | TO generates an alarm                 | TGn_TO_INTR        |
| TIMG_WDT_INT               | The watchdog timer generates an alarm | TGn_WDT_INTR       |
```