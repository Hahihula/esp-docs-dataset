

```markdown
## 3.6.1 Programming Procedures for GDMA's Transmit Channel

To transmit data, GDMA's transmit channel should be configured by software as follows:

1. Set `GDMA_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer.
2. Load an outlink, and configure `GDMA_OUTLINK_ADDR_CHn` with address of the first transmit descriptor.
3. Configure `GDMA_PERI_OUT_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 3.4-1.
4. Set `GDMA_OUTLINK_START_CHn` to enable GDMA's transmit channel for data transfer.
5. Configure and enable the corresponding peripheral. See details in individual chapters of these peripherals.
6. Wait for the `GDMA_OUT_TOTAL_EOF_CHn_INT` interrupt, which indicates the completion of data transfer.

## 3.6.2 Programming Procedures for GDMA's Receive Channel

To receive data, GDMA's receive channel should be configured by software as follows:

1. Set `GDMA_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer.
2. Load an inlink, and configure `GDMA_INLINK_ADDR_CHn` with address of the first receive descriptor.
3. Configure `GDMA_PERI_IN_SEL_CHn` with the value corresponding to the peripheral to be connected, as shown in Table 3.4-1.
4. Set `GDMA_INLINK_START_CHn` to enable GDMA's receive channel for data transfer.
5. Configure and enable the corresponding peripheral. See details in individual chapters of these peripherals.

## 3.6.3 Programming Procedures for Memory-to-Memory Transfer

To transfer data from one memory location to another, GDMA should be configured by software as follows:

1. Set `GDMA_OUT_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's transmit channel and FIFO pointer.
2. Set `GDMA_IN_RST_CHn` first to 1 and then to 0, to reset the state machine of GDMA's receive channel and FIFO pointer.
3. Load an outlink, and configure `GDMA_OUTLINK_ADDR_CHn` with address of the first transmit descriptor.
4. Load an inlink, and configure `GDMA_INLINK_ADDR_CHn` with address of the first receive descriptor.
5. Set `GDMA_MEM_TRANS_EN_CHn` to enable memory-to-memory transfer.
6. Set `GDMA_OUTLINK_START_CHn` to enable GDMA's transmit channel for data transfer.
7. Set `GDMA_INLINK_START_CHn` to enable GDMA's receive channel for data transfer.
```