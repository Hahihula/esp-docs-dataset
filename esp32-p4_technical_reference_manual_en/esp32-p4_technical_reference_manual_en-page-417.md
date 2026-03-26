

```markdown
## 6.7.4 Configurations for 2D-DMA's Receive Channel

To receive data, 2D-DMA's receive channel should be configured by software as follows:

1. Set `DMA2D_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of 2D-DMA's receive channel and FIFO pointer.
2. Load an inlink, and configure `DMA2D_INLINK_ADDR_CHn` with address of the first receive descriptor.
3. Configure `DMA2D_IN_PERI_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 6.4-3.
4. Set `DMA2D_INLINK_START_CHn` to enable 2D-DMA's receive channel for data transfer.
5. Configure and enable the corresponding peripheral. See details in individual chapters of these peripherals.
6. Wait for `DMA2D_IN_SUC_EOF_CHn_INT` interrupt, which indicates that an image has been received.

## 6.7.5 Configurations for Memory-to-Memory Transfer

To transfer data from one memory location to another, 2D-DMA should be configured by software as follows:

1. Set `DMA2D_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of 2D-DMA's transmit channel and FIFO pointer.
2. Set `DMA2D_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of 2D-DMA's receive channel and FIFO pointer.
3. Load an outlink, and configure `DMA2D_OUTLINK_ADDR_CHn` with address of the first transmit descriptor.
4. Load an inlink, and configure `DMA2D_INLINK_ADDR_CHn` with address of the first receive descriptor.
5. Configure `DMA2D_PERI_OUT_SEL_CHn` with any value corresponding to Dummy-n (see Table 6.4-2).
6. Configure `DMA2D_PERI_IN_SEL_CHn` with any value corresponding to Dummy-n (see Table 6.4-3).
7. Set `DMA2D_IN_MEM_TRANS_EN_CHn` to enable memory-to-memory transfer.
8. Set `DMA2D_OUTLINK_START_CHn` to enable 2D-DMA's transmit channel for data transfer.
9. Set `DMA2D_INLINK_START_CHn` to enable 2D-DMA's receive channel for data transfer.
10. Wait for `DMA2D_IN_SUC_EOF_CHn_INT` interrupt, which indicates that a data transaction has been completed.

## 6.7.6 Configurations for Channel Priority and Weight

The priority arbitration can be configured as follows:

1. Configure the channel priority for TX and RX respectively via `DMA2D_OUT_ARB_PRIORITY_CHn` and `DMA2D_IN_ARB_PRIORITY_CHn`.

The weight arbitration can be configured as follows:

1. Configure the time slot for TX and RX respectively via `DMA2D_OUT_ARB_TIMEOUT_NUM` and `DMA2D_IN_ARB_TIMEOUT_NUM`.
```