

```markdown
| SOC_ETM_CHn_EVT_ID | Selected Event                                                                 | Peripheral Generating This Event |
|--------------------|---------------------------------------------------------------------------------|----------------------------------|
| 201                | GDMA_AXI_EVT_IN_FIFO_EMPTY_CH1                                                 |                                  |
| 202                | GDMA_AXI_EVT_IN_FIFO_EMPTY_CH2                                                 |                                  |
| 203                | GDMA_AXI_EVT_IN_FIFO_FULL_CHO                                                  |                                  |
| 204                | GDMA_AXI_EVT_IN_FIFO_FULL_CH1                                                  |                                  |
| 205                | GDMA_AXI_EVT_IN_FIFO_FULL_CH2                                                  |                                  |
| 206                | GDMA_AXI_EVT_OUT_DONE_CHO                                                       |                                  |
| 207                | GDMA_AXI_EVT_OUT_DONE_CH1                                                       |                                  |
| 208                | GDMA_AXI_EVT_OUT_DONE_CH2                                                       |                                  |
| 209                | GDMA_AXI_EVT_OUT_EOF_CHO                                                        |                                  |
| 210                | GDMA_AXI_EVT_OUT_EOF_CH1                                                        |                                  |
| 211                | GDMA_AXI_EVT_OUT_EOF_CH2                                                        |                                  |
| 212                | GDMA_AXI_EVT_OUT_TOTAL_EOF_CHO                                                 |                                  |
| 213                | GDMA_AXI_EVT_OUT_TOTAL_EOF_CH1                                                 |                                  |
| 214                | GDMA_AXI_EVT_OUT_TOTAL_EOF_CH2                                                 |                                  |
| 215                | GDMA_AXI_EVT_OUT_FIFO_EMPTY_CH0                                                |                                  |
| 216                | GDMA_AXI_EVT_OUT_FIFO_EMPTY_CH1                                                |                                  |
| 217                | GDMA_AXI_EVT_OUT_FIFO_EMPTY_CH2                                                |                                  |
| 218                | GDMA_AXI_EVT_OUT_FIFO_FULL_CHO                                                 |                                  |
| 219                | GDMA_AXI_EVT_OUT_FIFO_FULL_CH1                                                 |                                  |
| 220                | GDMA_AXI_EVT_OUT_FIFO_FULL_CH2                                                 |                                  |
| 221                | PMU_EVT_SLEEP_WAKEUP                                                            | PMU                             |
| 222                | DMA2D_EVT_IN_DONE_CHO                                                           | 2D-DMA Controller (2D-DMA)       |
| 223                | DMA2D_EVT_IN_DONE_CH1                                                           |                                  |
| 224                | DMA2D_EVT_IN_SUC_EOF_CHO                                                        |                                  |
| 225                | DMA2D_EVT_IN_SUC_EOF_CH1                                                        |                                  |
| 226                | DMA2D_EVT_OUT_DONE_CHO                                                          |                                  |
| 227                | DMA2D_EVT_OUT_DONE_CH1                                                          |                                  |
| 228                | DMA2D_EVT_OUT_DONE_CH2                                                          |                                  |
| 229                | DMA2D_EVT_OUT_EOF_CHO                                                           |                                  |
| 230                | DMA2D_EVT_OUT_EOF_CH1                                                           |                                  |
| 231                | DMA2D_EVT_OUT_EOF_CH2                                                           |                                  |
| 232                | DMA2D_EVT_OUT_TOTAL_EOF_CHO                                                     |                                  |
| 233                | DMA2D_EVT_OUT_TOTAL_EOF_CH1                                                     |                                  |
| 234                | DMA2D_EVT_OUT_TOTAL_EOF_CH2                                                     |                                  |
```

Whenever any of these events occurs, the corresponding peripheral generates a pulse signal. As soon as the pulse signal is high, the event is considered as being received.

For more detailed descriptions of an event, please refer to the chapter for the peripheral generating this event.

### 13.3.3 Tasks

An ETM channel can be set up to map its event to one of the tasks by configuring the `SOC_ETM_CHn_TASK_ID` field. Table13.3-2 shows the configuration values of `SOC_ETM_CHn_TASK_ID` and