

```markdown
5. Configure and enable the corresponding peripheral (SPI2, UHClO (UART0 or UART1), I2S, AES, SHA, and ADC). See details in individual chapters of these peripherals;

## 2.6.4 Programming Procedures for Memory-to-Memory Transfer

To transfer data from one memory location to another, GDMA should be configured by software as follows:

1. Set `GDMA_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer;
2. Set `GDMA_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer;
3. Load an outlink, and configure `GDMA_OUTLINK_ADDR_CHn` with address of the first transmit descriptor;
4. Load an inlink, and configure `GDMA_INLINK_ADDR_CHn` with address of the first receive descriptor;
5. Set `GDMA_MEM_TRANS_EN_CHn` to enable memory-to-memory transfer;
6. Set `GDMA_OUTLINK_START_CHn` to enable GDMA's transmit channel for data transfer;
7. Set `GDMA_INLINK_START_CHn` to enable GDMA's receive channel for data transfer;

8. If the suc_eof bit is set in a transmit descriptor, a `GDMA_IN_SUC_EOF_CHn_INT` interrupt will be triggered when the data segment corresponding to this descriptor has been transmitted.
```