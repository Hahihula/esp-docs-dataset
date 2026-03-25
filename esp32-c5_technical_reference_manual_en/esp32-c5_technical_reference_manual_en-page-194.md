

```markdown
- AHB_DMA_OUT_DONE_CHn_INT: Triggered when all data corresponding to a transmit descriptor has been sent via transmit channel n.
- AHB_DMA_OUT_EOF_CHn_INT: Triggered when the suc_eof bit in a transmit descriptor is 1 and data corresponding to this descriptor has been sent via transmit channel n. If AHB_DMA_OUT_EOF_MODE_CHn is 0, this interrupt will be triggered when the last byte of data corresponding to this descriptor enters GDMA's transmit channel; if AHB_DMA_OUT_EOF_MODE_CHn is 1, this interrupt is triggered when the last byte of data is taken from GDMA's transmit channel.
- AHB_DMA_OUT_DSCR_ERR_CHn_INT: Triggered when a transmit descriptor on transmit channel n fails any of the two descriptor checks.
- AHB_DMA_OUT_TOTAL_EOF_CHn_INT: Triggered when all data corresponding to a linked list (including multiple descriptors) has been sent via transmit channel n.
- AHB_DMA_OUTFIFO_OVF_CHn_INT: Triggered when the TX FIFO of GDMA overflows.
- AHB_DMA_OUTFIFO_UDE_CHn_INT: Triggered when the TX FIFO of GDMA underflows.
- AHB_DMA_OUT_AHBINF_RESP_ERR_CHn_INT: Triggered when GDMA transmit channel n performs a data transfer on the AHB bus and an error response is received during the transfer.

## 5.7 Programming Procedures

The clock gating for GDMA can be configured via `PCR_GDMA_CLK_EN`, and is enabled by default. GDMA can be reset by configuring `PCR_GDMA_RST_EN`.

### 5.7.1 Programming Procedures for GDMA's Transmit Channel

To transmit data, GDMA's transmit channel should be configured by software as follows:

1. Set `AHB_DMA_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer.
2. Load an outlink, and configure `AHB_DMA_OUTLINK_ADDR_CHn` with address of the first transmit descriptor.
3. Configure `AHB_DMA_PERI_OUT_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 5.4-1.
4. Set `AHB_DMA_OUTLINK_START_CHn` to enable GDMA's transmit channel for data transfer.
5. Configure and enable the corresponding peripheral. See details in the individual chapter for the corresponding peripheral.
6. Wait for the `AHB_DMA_OUT_TOTAL_EOF_CHn_INT` interrupt, which indicates the completion of data transfer.

### 5.7.2 Programming Procedures for GDMA's Receive Channel

To receive data, GDMA's receive channel should be configured by software as follows:

1. Set `AHB_DMA_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer.
```