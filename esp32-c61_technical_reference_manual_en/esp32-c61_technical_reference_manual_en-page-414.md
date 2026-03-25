

```markdown
| SOC_ETM_CHn_TASK_ID | Mapped Task                                                                                      | Peripheral Receiving This Task              |
|---------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| 89                  | TGO_TASK_CNT_RELOAD_TIMER1                                                                       |                                              |
| 90                  | TGO_TASK_CNT_CAP_TIMER1                                                                          |                                              |
| 91                  | TG1_TASK_CNT_START_TIMERO                                                                        | General-purpose timer group 1                |
| 92                  | TG1_TASK_ALARM_START_TIMERO                                                                      |                                              |
| 93                  | TG1_TASK_CNT_STOP_TIMERO                                                                         |                                              |
| 94                  | TG1_TASK_CNT_RELOAD_TIMERO                                                                       |                                              |
| 95                  | TG1_TASK_CNT_CAP_TIMERO                                                                          |                                              |
| 96                  | TG1_TASK_CNT_START_TIMER1                                                                        |                                              |
| 97                  | TG1_TASK_ALARM_START_TIMER1                                                                      |                                              |
| 98                  | TG1_TASK_CNT_STOP_TIMER1                                                                         |                                              |
| 99                  | TG1_TASK_CNT_RELOAD_TIMER1                                                                       |                                              |
| 100                 | TG1_TASK_CNT_CAP_TIMER1                                                                          |                                              |
| 101                 | ADC_TASK_SAMPLEO                                                                                  | ADC Controller                              |
| 103                 | ADC_TASK_STARTO                                                                                  |                                              |
| 104                 | ADC_TASK_STOPO                                                                                   |                                              |
| 109                 | TMPSENSR_TASK_START_SAMPLE                                                                       | Temperature Sensor                           |
| 110                 | TMPSENSR_TASK_STOP_SAMPLE                                                                        |                                              |
| 111                 | I2SO_TASK_START_RX                                                                                | I2S                                         |
| 112                 | I2SO_TASK_START_TX                                                                                |                                              |
| 113                 | I2SO_TASK_STOP_RX                                                                                 |                                              |
| 114                 | I2SO_TASK_STOP_TX                                                                                 |                                              |
| 125                 | GDMA_TASK_IN_START_CHO                                                                            | GDMA Controller (GDMA)                       |
| 126                 | GDMA_TASK_IN_START_CH1                                                                           |                                              |
| 128                 | GDMA_TASK_OUT_START_CHO                                                                          |                                              |
| 129                 | GDMA_TASK_OUT_START_CH1                                                                          |                                              |
| 131                 | PMU_TASK_SLEEP_REQ                                                                                | PMU                                         |

When a channel receives a valid event pulse signal, it generates the mapped task pulse signal.

For more detailed descriptions of a task, please refer to the chapter for the peripheral receiving this task.

Events from different channels can be optionally mapped to the same task. For example, field `SOC_ETM_CHn_TASK_ID` of multiple channels can be configured with the same value, and field `SOC_ETM_CHn_EVT_ID` can be configured with the same or different values. In this case, when the event received by any of the channels is valid, the task will be generated. If events received by multiple channels are valid at the same time, the task will be generated only once.

### 10.3.4 Event and Task Status

The ETM module supports checking the status of events and tasks by reading registers as follows:

*   Event status can be checked by reading the `SOC_ETM_EVT_STn_REG` register. If the field corresponding to an event is 1, it indicates that the event has been received by ETM. Otherwise, it indicates that the event has not been received by ETM. The fields in the `SOC_ETM_EVT_STn_REG` register can be cleared by writing 1 to the corresponding fields in the `SOC_ETM_EVT_STn_CLR_REG` register.
```