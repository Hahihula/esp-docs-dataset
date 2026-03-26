

```markdown
3. Load an outlink, and configure AHB/AXI_DMA_OUTLINK_ADDR_CHn with address of the first transmit descriptor.
4. Load an inlink, and configure AHB/AXI_DMA_INLINK_ADDR_CHn with address of the first receive descriptor.
5. Set AHB/AXI_DMA_MEM_TRANS_EN_CHn to enable memory-to-memory transfer.
6. Set AHB/AXI_DMA_OUTLINK_START_CHn to enable GDMA's transmit channel for data transfer.
7. Set AHB/AXI_DMA_INLINK_START_CHn to enable GDMA's receive channel for data transfer.
8. If the suc_eof bit is set in a transmit descriptor, an AHB/AXI_DMA_IN_SUC_EOF_CHn_INT interrupt will be triggered when the data segment corresponding to this descriptor has been transmitted.

### 4.7.4 Programming Procedures for Channel Priority and Weight

The priority arbitration can be configured as follows:

1. Configure the channel priority for TX and RX respectively via AHB/AXI_DMA_TX_PRI_CHn and AHB/AXI_DMA_RX_PRI_CHn.

The weight arbitration can be configured as follows:

1. Configure the time slot
   * GDMA-AHB: TX and RX share the same time slot configured by AHB/AHB_DMA_ARB_TIMEOUT.
   * GDMA-AXI: TX and RX use independent time slots configured by AXI_DMA_ARB_TIMEOUT_TX and AXI_DMA_ARB_TIMEOUT_RX.

2. Configure the number of tokens for TX and RX respectively via AHB/AXI_DMA_TX_CH_ARB_WEIGH_CHn and AHB/AXI_DMA_RX_CH_ARB_WEIGH_CHn.

3. Enable weight arbitration optimization for TX and RX respectively by clearing AHB/AXI_DMA_TX_ARB_WEIGH_OPT_DIR_CHn and AHB/AXI_DMA_RX_ARB_WEIGH_OPT_DIR_CHn.

4. Enable the arbitration:
   * GDMA-AHB: Enable the arbitration for both TX and RX by setting AHB_DMA_WEIGHT_EN.
   * GDMA-AXI: Enable the arbitration for TX and RX respectively by setting AXI_DMA_WEIGHT_EN_TX and AXI_DMA_WEIGHT_EN_RX.

### 4.7.5 Programming Procedures for CRC Calculation

The CRC calculation registers can be configured as follows:

1. Configure which bits in crc_tmp and data are used in the matrix via
   AHB/AXI_DMA_TX_CRC_EN_ADDR_CHn, AHB/AXI_DMA_TX_CRC_DATA_EN_ADDR_CHn,
   AHB/AXI_DMA_TX_CRC_EN_WR_DATA_CHn, and AHB/AXI_DMA_TX_CRC_DATA_EN_WR_DATA_CHn.

2. Latch the values of the above four fields by first writing 1 and then 0 to
   AHB/AXI_DMA_TX_CRC_LATCH_FLGCHA_CHn. Then the configuration for a row is complete.

3. Repeat Step 1 and Step 2 until all rows in the matrix are set up, and then start DMA transfer.
```