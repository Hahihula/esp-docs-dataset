

```markdown
2. Set `AHB_DMA_IN_RST_Ch` first to 1 and then to 0, to reset the state machine of GDMA’s receive channel and FIFO pointer.
3. Load an outlink, and configure `AHB_DMA_OUTLINK_ADDR_Ch` with address of the first transmit descriptor.
4. Load an inlink, and configure `AHB_DMA_INLINK_ADDR_Ch` with address of the first receive descriptor.
5. Set `AHB_DMA_MEM_TRANS_EN_Ch` to enable memory-to-memory transfer.
6. Configure `AHB_DMA_PERI_IN_SEL_Ch` and `AHB_DMA_PERI_OUT_SEL_Ch` to the same “Dummy” value.
7. Set `AHB_DMA_OUTLINK_START_Ch` to enable GDMA’s transmit channel for data transfer.
8. Set `AHB_DMA_INLINK_START_Ch` to enable GDMA’s receive channel for data transfer.
9. If the `suc_eof` bit is set in a transmit descriptor, an `AHB_DMA_IN_SUC_EOF_Ch_INT` interrupt will be triggered when the data segment corresponding to this descriptor has been transmitted.

## 3.7.4 Programming Procedures for Channel Priority and Weight

The priority arbitration can be configured as follows:

1. Configure the channel priority for TX and RX respectively via `AHB_DMA_TX_PRI_Ch` and `AHB_DMA_RX_PRI_Ch`.

The weight arbitration can be configured as follows:

1. Configure the time slot for TX and RX respectively via `AHB_DMA_ARB_TIMEOUT_TX` and `AHB_DMA_ARB_TIMEOUT_RX`.
2. Configure the number of tokens for TX and RX respectively via `AHB_DMA_TX_CH_ARB_WEIGH_Ch` and `AHB_DMA_RX_CH_ARB_WEIGH_Ch`.
3. Enable weight arbitration optimization for TX and RX respectively by clearing `AHB_DMA_TX_ARB_WEIGH_OPT_DIR_Ch` and `AHB_DMA_RX_ARB_WEIGH_OPT_DIR_Ch`.
4. Enable the arbitration for TX and RX respectively by setting `AHB_DMA_WEIGHT_EN_TX` and `AHB_DMA_WEIGHT_EN_RX`.
```