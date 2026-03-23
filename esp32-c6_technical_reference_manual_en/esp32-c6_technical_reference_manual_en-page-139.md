
```markdown
- GDMA_IN_ERR_EOF_CHn_INT: Triggered when an error is detected in the data segment corresponding to a descriptor received via receive channel n. This interrupt is used only for UHCI peripheral (UART0 or UART1) or PARLIO.
- GDMA_IN_SUC_EOF_CHn_INT: Triggered when the suc_eof bit in a receive descriptor is 1 and the data corresponding to this receive descriptor has been received via receive channel n.
- GDMA_IN_DONE_CHn_INT: Triggered when all data corresponding to a receive descriptor has been received via receive channel n.
- GMA_OUTFIFO_OVF_CHn_INT: Triggered when the TX FIFO of GDMA overflows.
- GDMA_OUTFIFO_UDF_CHn_INT: Triggered when the TX FIFO of GDMA underflows.
- GDMA_OUT_DSCR_ERR_CHn_INT: Triggered when an error is detected in a transmit descriptor on transmit channel n.
- GDMA_OUT_EOF_CHn_INT: Triggered when EOF in a transmit descriptor is 1 and data corresponding to this descriptor has been sent via transmit channel n. If GDMA_OUT_EOF_MODE_CHn is 0, this interrupt will be triggered when the last byte of data corresponding to this descriptor enters GDMA's transmit channel; if GDMA_OUT_EOF_MODE_CHn is 1, this interrupt is triggered when the last byte of data is taken from GDMA's transmit channel.
- GDMA_OUT_DONE_CHn_INT: Triggered when all data corresponding to a transmit descriptor has been sent via transmit channel n.
- GDMA_OUT_TOTAL_EOF_CHn_INT: Triggered when all data corresponding to a linked list (including multiple descriptors) has been sent via transmit channel n.

## 4.6 Programming Procedures

The clock gating for GDMA can be configured via PCR_GDMA_CLK_EN, and is enabled by default. GDMA can be reset by configuring PCR_GDMA_RST_EN.

### 4.6.1 Programming Procedures for GDMA's Transmit Channel

To transmit data, GDMA's transmit channel should be configured by software as follows:

1. Set GDMA_OUT_RST_CHn first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer.
2. Load an outlink, and configure GDMA_OUTLINK_ADDR_CHn with address of the first transmit descriptor.
3. Configure GDMA_PERI_OUT_SEL_CHn with the value corresponding to the peripheral to be connected, as shown in Table 4.4-1.
4. Set GDMA_OUTLINK_START_CHn to enable GDMA's transmit channel for data transfer.
5. Configure and enable the corresponding peripheral (SPI2, UHCI (UART0 or UART1), I2S, AES, SHA, and ADC). See details in individual chapters of these peripherals.
6. Wait for GDMA_OUT_TOTAL_EOF_CHn_INT interrupt, which indicates the completion of data transfer.
```