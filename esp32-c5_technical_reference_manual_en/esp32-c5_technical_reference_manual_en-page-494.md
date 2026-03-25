

```markdown
| SOC_ETM_CHn_EVT_ID | Selected Event                                 | Peripheral Generating This Event          |
|--------------------|------------------------------------------------|--------------------------------------------|
| 113                | ULP_EVT_START_INTR                            |                                            |
| 114                | RTC_EVT_TICK                                  | RTC Timer                                 |
| 115                | RTC_EVT_OVF                                   |                                            |
| 116                | RTC_EVT_CMP                                   |                                            |
| 117                | GDMA_EVT_IN_DONE_CHO                          | GDMA Controller (GDMA)                     |
| 118                | GDMA_EVT_IN_DONE_CH1                          |                                            |
| 119                | GDMA_EVT_IN_DONE_CH2                          |                                            |
| 120                | GDMA_EVT_IN_SUC_EOFCHO                        |                                            |
| 121                | GDMA_EVT_IN_SUC_EOF_CH1                       |                                            |
| 122                | GDMA_EVT_IN_SUC_EOF_CH2                       |                                            |
| 123                | GDMA_EVT_IN_FIFO_EMPTYCHO                     |                                            |
| 124                | GDMA_EVT_IN_FIFO_EMPTY_CH1                    |                                            |
| 125                | GDMA_EVT_IN_FIFO_EMPTY_CH2                    |                                            |
| 126                | GDMA_EVT_IN_FIFO_FULLCHO                      |                                            |
| 127                | GDMA_EVT_IN_FIFO_FULL_CH1                     |                                            |
| 128                | GDMA_EVT_IN_FIFO_FULL_CH2                     |                                            |
| 129                | GDMA_EVT_OUT_DONECHO                          |                                            |
| 130                | GDMA_EVT_OUT_DONE_CH1                         |                                            |
| 131                | GDMA_EVT_OUT_DONE_CH2                         |                                            |
| 132                | GDMA_EVT_OUT_EOFCHO                           |                                            |
| 133                | GDMA_EVT_OUT_EOF_CH1                          |                                            |
| 134                | GDMA_EVT_OUT_EOF_CH2                          |                                            |
| 135                | GDMA_EVT_OUT_TOTAL_EOFCHO                     |                                            |
| 136                | GDMA_EVT_OUT_TOTAL_EOF_CH1                    |                                            |
| 137                | GDMA_EVT_OUT_TOTAL_EOF_CH2                    |                                            |
| 138                | GDMA_EVT_OUT_FIFO_EMPTYCHO                    |                                            |
| 139                | GDMA_EVT_OUT_FIFO_EMPTY_CH1                   |                                            |
| 140                | GDMA_EVT_OUT_FIFO_EMPTY_CH2                   |                                            |
| 141                | GDMA_EVT_OUT_FIFO_FULLCHO                     |                                            |
| 142                | GDMA_EVT_OUT_FIFO_FULL_CH1                    |                                            |
| 143                | GDMA_EVT_OUT_FIFO_FULL_CH2                    |                                            |
| 144                | PMU_EVT_SLEEP_WEEKUP                          | PMU                                       |
```

Whenever any of these events occurs, the corresponding peripheral generates a pulse signal. As soon as the pulse signal is high, the event is considered as being received.

For more detailed descriptions of an event, please refer to the chapter for the peripheral generating this event.

## 12.3.3 Tasks

An ETM channel can be set up to map its event to one of the tasks by configuring the `SOC_ETM_CHn_TASK_ID` field. Table 12.3-2 shows the configuration values of `SOC_ETM_CHn_TASK_ID` and their corresponding tasks.
```