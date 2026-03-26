

```markdown
Register 4.112. AXI_DMA_INFIFO_STATUS_CHn_REG (n: 0-2) (0x0018+0x68*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1 |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

AXI_DMA_INFIFO_L3_FULL_CHn Represents whether L3 RX FIFO is full.
O: Not Full
1: Full
(RO)

AXI_DMA_INFIFO_L3_EMPTY_CHn Represents whether L3 RX FIFO is empty.
O: Not empty
1: Empty
(RO)

AXI_DMA_INFIFO_L3_CNT_CHn Represents the number of data bytes in L3 RX FIFO for RX channel n. (RO)

AXI_DMA_INFIFO_L3_UDF_CHn Represents whether L3 RX FIFO underflows.
O: No underflow
1: Underflow
(RO)

AXI_DMA_INFIFO_L3_OVF_CHn Represents whether L3 RX FIFO overflows.
O: No overflow
1: Overflow
(RO)

AXI_DMA_INFIFO_L1_FULL_CHn Represents whether L1 RX FIFO is full.
O: Not Full
1: Full
(RO)

AXI_DMA_INFIFO_L1_EMPTY_CHn Represents whether L1 RX FIFO is empty.
O: Not empty
1: Empty
(RO)

AXI_DMA_INFIFO_L1_UDF_CHn Represents whether L1 RX FIFO underflows.
O: No underflow
1: Underflow
(RO)
```