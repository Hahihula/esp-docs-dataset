

```markdown
Register 4.119. AXI_DMA_OUTFIFO_STATUS_CHn_REG (n: 0-2) (0x0150+0x68*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | O  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0 |
|     | Reset |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

AXI_DMA_OUTFIFO_L3_FULL_CHn Represents whether L3 TX FIFO is full.
O: Not Full
1: Full
(RO)

AXI_DMA_OUTFIFO_L3_EMPTY_CHn Represents whether L3 TX FIFO is empty.
O: Not empty
1: Empty
(RO)

AXI_DMA_OUTFIFO_L3_CNT_CHn Represents the number of data bytes in L3 TX FIFO for TX channel n. (RO)

AXI_DMA_OUTFIFO_L3_UDF_CHn Represents whether L3 TX FIFO underflows.
O: No underflow
1: Underflow
(RO)

AXI_DMA_OUTFIFO_L3_OVF_CHn Represents whether L3 TX FIFO overflows.
O: No overflow
1: Overflow
(RO)

AXI_DMA_OUTFIFO_L1_FULL_CHn Represents whether L1 TX FIFO is full.
O: Not Full
1: Full
(RO)

AXI_DMA_OUTFIFO_L1_EMPTY_CHn Represents whether L1 TX FIFO is empty.
O: Not empty
1: Empty
(RO)

AXI_DMA_OUTFIFO_L1_UDF_CHn Represents whether L1 TX FIFO underflows.
O: No underflow
1: Underflow
(RO)
```