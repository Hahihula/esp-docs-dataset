

```markdown
Register 6.47. DMA2D_OUTFIFO_STATUS_CHn_REG (n: 0-3) (0x0014+0x100*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     | 0  | 0  | 0  | 0x0| 1  | 0  | 0x0| 1  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 0  | xOx| 1  | 0  | (reserved) | DMA2D_OUTFIFO_EMPTY_L2_CHn | DMA2D_OUTFIFO_FULL_L2_CHn |
```

DMA2D_OUTFIFO_FULL_L2_CHn Represents whether the L2 TX FIFO for TX channel n is full.

O: Not full
1: Full
(RO)

DMA2D_OUTFIFO_EMPTY_L2_CHn Represents whether the L2 TX FIFO for TX channel n is empty.

O: Not empty
1: Empty
(RO)

DMA2D_OUTFIFO_CNT_L2_CHn Represents the number of data bytes in L2 TX FIFO for TX channel n. (RO)

DMA2D_OUT_REMAIN_UNDER_1B_CHn Reserved. (RO)
DMA2D_OUT_REMAIN_UNDER_2B_CHn Reserved. (RO)
DMA2D_OUT_REMAIN_UNDER_3B_CHn Reserved. (RO)
DMA2D_OUT_REMAIN_UNDER_4B_CHn Reserved. (RO)
DMA2D_OUT_REMAIN_UNDER_5B_CHn Reserved. (RO)
DMA2D_OUT_REMAIN_UNDER_6B_CHn Reserved. (RO)
DMA2D_OUT_REMAIN_UNDER_7B_CHn Reserved. (RO)
DMA2D_OUT_REMAIN_UNDER_8B_CHn Reserved. (RO)

DMA2D_OUTFIFO_FULL_L1_CHn Represents whether the L1 TX FIFO for TX channel n is full.

O: Not full
1: Full
(RO)

DMA2D_OUTFIFO_EMPTY_L1_CHn Represents whether the L1 TX FIFO for TX channel n is empty.

O: Not empty
1: Empty
(RO)

DMA2D_OUTFIFO_CNT_L1_CHn Represents the number of data bytes in L1 TX FIFO for TX channel n. (RO)
```