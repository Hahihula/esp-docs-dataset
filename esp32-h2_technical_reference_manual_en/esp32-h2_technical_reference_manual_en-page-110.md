

```markdown
tasks. This section introduces the ETM tasks and events related to GDMA. For more information, please refer to Chapter 10 Event Task Matrix (SOC_ETM).

GDMA can receive the following ETM tasks:

*   `GDMA_TASK_IN_START_CHn`: Enables the corresponding RX channel n for data transfer.
*   `GDMA_TASK_OUT_START_CHn`: Enables the corresponding TX channel n for data transfer.

Note:
Above ETM tasks can achieve the same functions as CPU configuring GDMA_INLINK_START_CHn and GDMA_OUTLINK_START_CHn. When GDMA_IN_ETM_EN_Chn or GDMA_OUT_ETM_EN_Chn is 1, only ETM tasks can be used to configure the transfer direction and enable the corresponding GDMA channel. When GDMA_IN_ETM_EN_Chn or GDMA_OUT_ETM_EN_Chn is 0, only CPU can be used to enable the corresponding GDMA channel.

GDMA can generate the following ETM events:

*   `GDMA_EVT_IN_DONE_CHn`: Indicates that the data has been received according to the receive descriptor via channel n.
*   `GDMA_EVT_IN_SUC_EOF_CHn`: Indicates that the data corresponding to a receive descriptor has been received via channel n and the EOF bit of this descriptor is 1.
*   `GDMA_EVT_IN_FIFO_EMPTY_CHn`: Indicates that the RX FIFO has become empty.
*   `GDMA_EVT_IN_FIFO_FULL_CHn`: Indicates that the RX FIFO has become full.
*   `GDMA_EVT_OUT_DONE_CHn`: Indicates that the data has been transmitted according to the transmit descriptor via channel n.
*   `GDMA_EVT_OUT_SUC_EOF_CHn`: Indicates that the data corresponding to a transmit descriptor has been transmitted or received via channel n and the EOF bit of this descriptor is 1.
*   `GDMA_EVT_OUT_TOTAL_EOF_CHn`: Indicates that the data corresponding to the last transmit descriptors has been sent via transmit channel n and the EOF bit of this descriptor is 1.
*   `GDMA_EVT_OUT_FIFO_EMPTY_CHn`: Indicates that the TX FIFO has become empty.
*   `GDMA_EVT_OUT_FIFO_FULL_CHn`: Indicates that the TX FIFO has become full.

In practical applications, GDMA's ETM events can trigger its own ETM tasks. For example, the GDMA_EVT_OUT_TOTAL_EOF_CH0 event can trigger the GDMA_TASK_IN_START_CH1 task, and in this way trigger a new round of GDMA operations.

## 3.5 GDMA Interrupts

GDMA on ESP32-H2 can generate the following 6 interrupt signals, and send them to Interrupt Matrix (INTMTX):

*   `GDMA_IN_CHO_INTR`
*   `GDMA_IN_CH1_INTR`
*   `GDMA_IN_CH2_INTR`

```
Espressif Systems
Submit Documentation Feedback
ESP32-H2 TRM (Version 1.1)
```