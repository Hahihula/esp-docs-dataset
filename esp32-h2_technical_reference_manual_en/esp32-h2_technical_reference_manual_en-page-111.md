

```markdown
- GDMA_OUT_CHO_INTR
- GDMA_OUT_CH1_INTR
- GDMA_OUT_CH2_INTR

The following interrupt sources trigger the GDMA_IN_CHn_INTR signals:

- DMA_INFIFO_OVF_CHn_INT: Triggered when the RX FIFO of GDMA overflows.
- GDMA_INFIFO_UDF_CHn_INT: Triggered when the RX FIFO of GDMA underflows.
- GDMA_IN_DSCR_EMPTY_CHn_INT: Triggered when the size of the buffer pointed by receive descriptors is smaller than the length of data to be received via receive channel n.
- GDMA_IN_DSCR_ERR_CHn_INT: Triggered when an error is detected in a receive descriptor on receive channel n.
- GDMA_IN_ERR_EOF_CHn_INT: Triggered when an error is detected in the data segment corresponding to a descriptor received via receive channel n. This interrupt is used only for UHCI peripheral (UART0 or UART1) or PARLIO.
- GDMA_IN_SUC_EOF_CHn_INT: Triggered when the suc_eof bit in a receive descriptor is 1 and the data corresponding to this receive descriptor has been received via receive channel n.
- GDMA_IN_DONE_CHn_INT: Triggered when all data corresponding to a receive descriptor has been received via receive channel n.

The following interrupt sources trigger the GDMA_OUT_CHn_INTR signals:

- GMA_OUTFIFO_OVF_CHn_INT: Triggered when the TX FIFO of GDMA overflows.
- GDMA_OUTFIFO_UDF_CHn_INT: Triggered when the TX FIFO of GDMA underflows.
- GDMA_OUT_TOTAL_EOF_CHn_INT: Triggered when all data corresponding to a linked list (including multiple descriptors) has been sent via transmit channel n.
- GDMA_OUT_DSCR_ERR_CHn_INT: Triggered when an error is detected in a transmit descriptor on transmit channel n.
- GDMA_OUT_EOF_CHn_INT: Triggered when EOF in a transmit descriptor is 1 and data corresponding to this descriptor has been sent via transmit channel n. If GDMA_OUT_EOF_MODE_CHn is 0, this interrupt will be triggered when the last byte of data corresponding to this descriptor enters GDMA's transmit channel; if GDMA_OUT_EOF_MODE_CHn is 1, this interrupt is triggered when the last byte of data is taken from GDMA's transmit channel.
- GDMA_OUT_DONE_CHn_INT: Triggered when all data corresponding to a transmit descriptor has been sent via transmit channel n.

## 3.6 Programming Procedures

The clock gating for GDMA can be configured via `PCR_GDMA_CLK_EN`, and is enabled by default. GDMA can be reset by configuring `PCR_GDMA_RST_EN`.
```