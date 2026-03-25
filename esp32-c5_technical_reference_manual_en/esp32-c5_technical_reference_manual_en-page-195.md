

```markdown
2. Load an inlink, and configure AHB_DMA_INLINK_ADDR_CHn with address of the first receive descriptor.
3. Configure AHB_DMA_PERI_IN_SEL_CHn with the value corresponding to the peripheral to be connected, as shown in Table 5.4-1.
4. Set AHB_DMA_INLINK_START_CHn to enable GDMA's receive channel for data transfer.
5. Configure and enable the corresponding peripheral. See details in the individual chapter for the corresponding peripheral.

## 5.7.3 Programming Procedures for Memory-to-Memory Transfer

To transfer data from one memory location to another, GDMA should be configured by software as follows:

1. Set AHB_DMA_OUT_RST_CHn first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer.
2. Set AHB_DMA_IN_RST_CHn first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer.
3. Load an outlink, and configure AHB_DMA_OUTLINK_ADDR_CHn with address of the first transmit descriptor.
4. Load an inlink, and configure AHB_DMA_INLINK_ADDR_CHn with address of the first receive descriptor.
5. Set AHB_DMA_MEM_TRANS_EN_CHn to enable memory-to-memory transfer.
6. Set AHB_DMA_OUTLINK_START_CHn to enable GDMA's transmit channel for data transfer.
7. Set AHB_DMA_INLINK_START_CHn to enable GDMA's receive channel for data transfer.
8. If the suc_eof bit is set in a transmit descriptor, an AHB_DMA_IN_SUC_EOF_CHn_INT interrupt will be triggered when the data segment corresponding to this descriptor has been transmitted.

## 5.7.4 Programming Procedures for Channel Priority and Weight

The priority arbitration can be configured as follows:

1. Configure the channel priority for TX and RX respectively via AHB_DMA_TX_PRI_CHn and AHB_DMA_RX_PRI_CHn.

The weight arbitration can be configured as follows:

1. Configure the time slot via AHB_DMA_ARB_TIMEOUT.
2. Configure the number of tokens for TX and RX respectively via AHB_DMA_TX_CH_ARB_WEIGH_CHn and AHB_DMA_RX_CH_ARB_WEIGH_CHn.
3. Enable weight arbitration optimization for TX and RX respectively by clearing AHB_DMA_TX_ARB_WEIGHT_OPT_DIR_CHn and AHB_DMA_RX_ARB_WEIGHT_OPT_DIR_CHn.
4. Enable the arbitration by setting AHB_DMA_WEIGHT_EN.
```