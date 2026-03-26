

```markdown
DMA2D_TASK_OUT_DSCR_READY_CHn: Allows transmit channel n to process the next descriptor.

Note:
In normal conditions, after finishing with the current descriptor if the next descriptor is available (i.e., the next descriptor address field is not zero), the 2D-DMA would process the next descriptor directly and reads/writes to the memory according to the descriptor’s configuration until all descriptors are processed. When DMA2D_IN_ETM_LOOP_EN_CHn or DMA2D_OUT_ETM_LOOP_EN_CHn is set, after finishing with the current descriptor, the 2D-DMA would not start processing the next descriptor until receiving the DMA2D_TASK_IN_DSCR_READY_CHn or
DMA2D_TASK_OUT_DSCR_READY_CHn task.
The DMA2D_TASK_IN_DSCR_READY_CHn or DMA2D_TASK_OUT_DSCR_READY_CHn task can be stored in the task buffer, which can cache at most four tasks. When the 2D-DMA receives this task but the current descriptor is not yet processed, it can cache the task. The depth of the task buffer is determined by DMA2D_IN_DSCR_TASK_MAX_CHn or DMA2D_OUT_DSCR_TASK_MAX_CHn.
When the task buffer exceeds its maximum capacity, it will trigger an DMA2D_IN_DSCR_TASK_OVF_CHn_INT or DMA2D_OUT_DSCR_TASK_OVF_CHn_INT interrupt.

2D-DMA can generate the following ETM events:
*   DMA2D_EVT_IN_DONE_CHn: Indicates that the data has been received according to the receive descriptor via channel n.
*   DMA2D_EVT_IN_SUC_EOF_CHn: Indicates that the data corresponding to a receive descriptor has been received via channel n and the Eof bit of this descriptor is 1.
*   DMA2D_EVT_OUT_DONE_CHn: Indicates that the data has been transmitted according to the transmit descriptor via channel n.
*   DMA2D_EVT_OUT_SUC_EOF_CHn: Indicates that the data corresponding to a transmit descriptor has been transmitted or received via channel n and the eof bit of this descriptor is 1.
*   DMA2D_EVT_OUT_TOTAL_EOF_CHn: Indicates that the data corresponding to the last transmit descriptors has been sent via transmit channel n and the eof bit of this descriptor is 1.

In practical applications, 2D-DMA’s ETM events can trigger its own ETM tasks. For example, the DMA2D_EVT_OUT_TOTAL_EOF_CHO event can trigger the DMA2D_TASK_IN_START_CH1 task, and in this way trigger a new round of 2D-DMA operations.
```

## 6.6 Interrupts

ESP32-P4’s 2D-DMA module can generate the following interrupt signals that will be sent to the **Interrupt Matrix**.

*   DMA2D_IN_CHO_INTR
*   DMA2D_IN_CH1_INTR
*   DMA2D_IN_CH2_INTR
*   DMA2D_OUT_CHO_INTR
*   DMA2D_OUT_CH1_INTR