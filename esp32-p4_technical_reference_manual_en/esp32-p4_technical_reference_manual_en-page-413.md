

```markdown
2D-DMA would respond to the transfer requests according to priority levels, and the channel with higher priority would get a response more timely.

* Weight arbitration:

  - Each channel is assigned a weight (i.e., the number of tokens) from 0 ~ 15. The 2D-DMA divides the AXI bus clock period into multiple time slots, and in each time slot, the number of transfers performed by a channel is determined by the number of its tokens. Every time a channel performs a data transfer, one of its tokens is spent. If all of its tokens have been spent in a time slot, then this channel's transfer request will no longer be responded to until the time slot expires, or until tokens of all channels have been spent and the new time slot starts.

  - If the number of tokens assigned to a channel is not zero, the 2D-DMA waits for this channel's tokens to be spent even if it does not have data transfer requests, and will not exit from this time slot ahead of expiration. This leads to a waste of bandwidth. Therefore, the 2D-DMA provides weight arbitration optimization. When this feature is enabled, a channel without data transfer requests will not be involved in the arbitration and its tokens will be ignored. When all channels no longer have transfer requests, the 2D-DMA arbiter exits from the current time slot before expiration. This way, the arbitration response is accelerated and the transfer efficiency is improved.

Note:

* If channels have the same weight but different priorities, on condition that the number of bytes to be transferred is the same and not large, channels with higher priorities would finish data transfers first.
* If channels have different priorities and weights, on condition that the number of bytes to be transferred is the same, channels with higher weights would be allocated more bandwidth and finish data transfers first.

## 6.5 Event Task Matrix Feature

The 2D-DMA controller on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows 2D-DMA's ETM tasks to be triggered by any peripherals' ETM events, or 2D-DMA's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to 2D-DMA. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

2D-DMA can receive the following ETM tasks:

* DMA2D_TASK_IN_START_CHn: Enables the corresponding receive channel n for data transfer.
* DMA2D_TASK_OUT_START_CHn: Enables the corresponding transmit channel n for data transfer.

Note:

Above ETM tasks can achieve the same functions as CPU configuring DMA2D_INLINK_START_CHn and DMA2D_OUTLINK_START_CHn. When DMA2D_IN_ETM_EN_CHn or DMA2D_OUT_ETM_EN_CHn is 1, only ETM tasks can be used to configure the transfer direction and enable the corresponding 2D-DMA channel. When DMA2D_IN_ETM_EN_CHn or DMA2D_OUT_ETM_EN_CHn is 0, only CPU can be used to enable the corresponding 2D-DMA channel.

* DMA2D_TASK_IN_DSCR_READY_CHn: Allows receive channel n to process the next descriptor.
```