

```markdown
requests, the GDMA arbiter exits from the current time slot before expiration. This way, the arbitration response is accelerated and the transfer efficiency is improved.

Note:
* If channels have the same weight but different priorities, on condition that the number of bytes to be transferred is the same and not large, channels with higher priorities would finish data transfers first.
* If channels have different priorities and weights, on condition that the number of bytes to be transferred is the same, channels with higher weights would be allocated more bandwidth and finish data transfers first.

## 3.5 Event Task Matrix Feature

The GDMA controller on ESP32-C61 supports the Event Task Matrix (ETM) function, which allows GDMA's ETM tasks to be triggered by any peripherals' ETM events, or GDMA's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to GDMA. For more information, please refer to Chapter 10 Event Task Matrix (ETM).

GDMA can receive the following ETM tasks:

* `GDMA_TASK_IN_START_CHn`: Enables the corresponding RX channel n for data transfer.
* `GDMA_TASK_OUT_START_CHn`: Enables the corresponding TX channel n for data transfer.

Note:
Above ETM tasks can achieve the same functions as CPU configuring AHB_DMA_INLINK_START_CHn and AHB_DMA_OUTLINK_START_CHn. When AHB_DMA_IN_ETM_EN_CHn or AHB_DMA_OUT_ETM_EN_CHn is 1, only ETM tasks can be used to configure the transfer direction and enable the corresponding GDMA channel. When AHB_DMA_IN_ETM_EN_CHn or AHB_DMA_OUT_ETM_EN_CHn is 0, only CPU can be used to enable the corresponding GDMA channel.

GDMA can generate the following ETM events:

* `GDMA_EVT_IN_DONE_CHn`: Indicates that the data has been received according to the receive descriptor via channel n.
* `GDMA_EVT_IN_SUC_EOF_CHn`: Indicates that the data corresponding to a receive descriptor has been received via channel n and the EOF bit of this descriptor is 1.
* `GDMA_EVT_IN_FIFO_EMPTY_CHn`: Indicates that the RX FIFO has become empty.
* `GDMA_EVT_IN_FIFO_FULL_CHn`: Indicates that the RX FIFO has become full.
* `GDMA_EVT_OUT_DONE_CHn`: Indicates that the data has been transmitted according to the transmit descriptor via channel n.
* `GDMA_EVT_OUT_EOF_CHn`: Indicates that the data corresponding to a transmit descriptor has been transmitted or received via channel n and the EOF bit of this descriptor is 1.
* `GDMA_EVT_OUT_TOTAL_EOF_CHn`: Indicates that the data corresponding to the last transmit descriptors has been sent via transmit channel n and the EOF bit of this descriptor is 1.
* `GDMA_EVT_OUT_FIFO_EMPTY_CHn`: Indicates that the TX FIFO has become empty.
```