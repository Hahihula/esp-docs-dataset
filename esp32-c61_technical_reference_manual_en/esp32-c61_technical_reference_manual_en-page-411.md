

```markdown
| SOC_ETM_CHn_EVT_ID | Selected Event                                 | Peripheral Generating This Event          |
|--------------------|------------------------------------------------|--------------------------------------------|
| 59                 | ADC_EVT_EQ_BELOW_THRESHO                       |                                            |
| 60                 | ADC_EVT_EQ_BELOW_THRESH1                       |                                            |
| 61                 | ADC_EVT_RESULT_DONEO                           |                                            |
| 62                 | ADC_EVT_STOPPEDO                               |                                            |
| 63                 | ADC_EVT_STARTEDO                               |                                            |
| 72                 | TMPSENSR_EVT_OVER_LIMIT                        | Temperature Sensor                         |
| 73                 | I2S0_EVT_RX_DONE                               | I2S                                        |
| 74                 | I2S0_EVT_TX_DONE                               |                                            |
| 75                 | I2S0_EVT_X_WORDS_RECEIVED                      |                                            |
| 76                 | I2S0_EVT_X_WORDS_SENT                          |                                            |
| 84                 | RTC_EVT_TICK                                   | RTC Timer                                  |
| 85                 | RTC_EVT_OVF                                    |                                            |
| 86                 | RTC_EVT_CMP                                    |                                            |
| 87                 | GDMA_EVT_IN_DONE_CHO                           | GDMA Controller (GDMA)                     |
| 88                 | GDMA_EVT_IN_DONE_CH1                           |                                            |
| 90                 | GDMA_EVT_IN_SUC_EOF_CHO                        |                                            |
| 91                 | GDMA_EVT_IN_SUC_EOF_CH1                        |                                            |
| 93                 | GDMA_EVT_IN_FIFO_EMPTYCHO                      |                                            |
| 94                 | GDMA_EVT_IN_FIFO_EMPTY_CH1                     |                                            |
| 96                 | GDMA_EVT_IN_FIFO_FULLCHO                       |                                            |
| 97                 | GDMA_EVT_IN_FIFO_FULL_CH1                      |                                            |
| 99                 | GDMA_EVT_OUT_DONE_CHO                          |                                            |
| 100                | GDMA_EVT_OUT_DONE_CH1                          |                                            |
| 102                | GDMA_EVT_OUT_EOFCHO                            |                                            |
| 103                | GDMA_EVT_OUT_EOF_CH1                           |                                            |
| 105                | GDMA_EVT_OUT_TOTAL_EOFCHO                      |                                            |
| 106                | GDMA_EVT_OUT_TOTAL_EOF_CH1                     |                                            |
| 108                | GDMA_EVT_OUT_FIFO_EMPTYCHO                     |                                            |
| 109                | GDMA_EVT_OUT_FIFO_EMPTY_CH1                    |                                            |
| 111                | GDMA_EVT_OUT_FIFO_FULLCHO                      |                                            |
| 112                | GDMA_EVT_OUT_FIFO_FULL_CH1                     |                                            |
| 114                | PMU_EVT_SLEEP_WEEKUP                           | PMU                                        |
```

Whenever any of these events occurs, the corresponding peripheral generates a pulse signal. As soon as the pulse signal is high, the event is considered as being received.

For more detailed descriptions of an event, please refer to the chapter corresponding to the peripheral that generates it.

## 10.3.3 Tasks

An ETM channel can be set up to map its event to one of the tasks by configuring the `SOC_ETM_CHn_TASK_ID` field. Table 10.3-2 shows the configuration values of `SOC_ETM_CHn_TASK_ID` and their corresponding tasks.
```