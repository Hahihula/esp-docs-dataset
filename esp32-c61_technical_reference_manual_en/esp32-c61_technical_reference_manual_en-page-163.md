

```markdown
- AHB_DMA_OUTFIFO_UF_CHn_INT: Triggered when the TX FIFO of GDMA underflows.
```

## 3.7 Programming Procedures

The clock gating for GDMA can be configured via `PCR_GDMA_CLK_EN`, and is enabled by default. GDMA can be reset by configuring `PCR_GDMA_RST_EN`.

### 3.7.1 Programming Procedures for GDMA’s Transmit Channel

To transmit data, GDMA’s transmit channel should be configured by software as follows:

1. Set `AHB_DMA_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA’s transmit channel and FIFO pointer.

2. Load an outlink, and configure `AHB_DMA_OUTLINK_ADDR_CHn` with address of the first transmit descriptor.

3. Configure `AHB_DMA_PERI_OUT_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 3.4-1.

4. Set `AHB_DMA_OUTLINK_START_CHn` to enable GDMA’s transmit channel for data transfer.

5. Configure and enable the corresponding peripheral. See details in the individual chapter for the corresponding peripheral.

6. Wait for the `AHB_DMA_OUT_TOTAL_EOF_CHn_INT` interrupt, which indicates the completion of data transfer.

### 3.7.2 Programming Procedures for GDMA’s Receive Channel

To receive data, GDMA’s receive channel should be configured by software as follows:

1. Set `AHB_DMA_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA’s receive channel and FIFO pointer.

2. Load an inlink, and configure `AHB_DMA_INLINK_ADDR_CHn` with address of the first receive descriptor.

3. Configure `AHB_DMA_PERI_IN_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 3.4-1.

4. Set `AHB_DMA_INLINK_START_CHn` to enable GDMA’s receive channel for data transfer.

5. Configure and enable the corresponding peripheral. See details in the individual chapter for the corresponding peripheral.

### 3.7.3 Programming Procedures for Memory-to-Memory Transfer

To transfer data from one memory location to another, GDMA should be configured by software as follows:

1. Set `AHB_DMA_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA’s transmit channel and FIFO pointer.
```