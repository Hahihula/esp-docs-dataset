

```markdown
- GDMA_OUT_DONE_CHn_INT: Triggered when all data corresponding to a transmit descriptor has been sent via transmit channel n.
- GDMA_IN_ERR_EOF_CHn_INT: Triggered when an error is detected in the data segment corresponding to a descriptor received via receive channel n. This interrupt is used only for UHCI0 peripheral (UART0 or UART1).
- GDMA_IN_SUC_EOF_CHn_INT: Triggered when the suc_eof bit in a receive descriptor is 1 and the data corresponding to this receive descriptor has been received via receive channel n.
- GDMA_IN_DONE_CHn_INT: Triggered when all data corresponding to a receive descriptor has been received via receive channel n.

## 2.6 Programming Procedures

### 2.6.1 Programming Procedure for GDMA Clock and Reset

GDMA's clock and reset should be configured as follows:

1. Set `SYSTEM_DMA_CLK_EN` to enable GDMA's clock;
2. Clear `SYSTEM_DMA_RST` to reset GDMA.

### 2.6.2 Programming Procedures for GDMA's Transmit Channel

To transmit data, GDMA's transmit channel should be configured by software as follows:

1. Set `GDMA_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer;
2. Load an outlink, and configure `GDMA_OUTLINK_ADDR_CHn` with address of the first transmit descriptor;
3. Configure `GDMA_PERI_OUT_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 2.4-1;
4. Set `GDMA_OUTLINK_START_CHn` to enable GDMA's transmit channel for data transfer;
5. Configure and enable the corresponding peripheral (SPI2, UHCI0 (UART0 or UART1), I2S, AES, SHA, and ADC). See details in individual chapters of these peripherals;
6. Wait for `GDMA_OUT_TOTAL_EOF_CHn_INT` interrupt, which indicates the completion of data transfer.

### 2.6.3 Programming Procedures for GDMA's Receive Channel

To receive data, GDMA's receive channel should be configured by software as follows:

1. Set `GDMA_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer;
2. Load an inlink, and configure `GDMA_INLINK_ADDR_CHn` with address of the first receive descriptor;
3. Configure `GDMA_PERI_IN_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 2.4-1;
4. Set `GDMA_INLINK_START_CHn` to enable GDMA's receive channel for data transfer;
```