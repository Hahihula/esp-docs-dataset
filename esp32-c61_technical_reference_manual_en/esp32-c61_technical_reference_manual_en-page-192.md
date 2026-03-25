

```markdown
Register 3.37. AHB_DMA_OUTFIFO_STATUS_CHn_REG (n: 0-1) (0x00D8+0xC0*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 1  | 0 |
|     | (reserved) | AHB_DMA_OUT_REMAIN_UNDER_4B_CHn | AHB_DMA_OUT_REMAIN_UNDER_3B_CHn | AHB_DMA_OUT_REMAIN_UNDER_2B_CHn | AHB_DMA_OUT_REMAIN_UNDER_1B_CHn | (reserved) | AHB_DMA_OUTFIFO_CNT_Chn | AHB_DMA_OUTFIFO_FULL_Chn | AHB_DMA_OUTFIFO_EMPTY_Chn |
```

AHB_DMA_OUTFIFO_FULL_Chn Represents whether L1 TX FIFO is full.

O: Not Full
1: Full
(RO)

AHB_DMA_OUTFIFO_EMPTY_Chn Represents whether L1 TX FIFO is empty.

O: Not empty
1: Empty
(RO)

AHB_DMA_OUTFIFO_CNT_Chn Represents the number of data bytes in L1 TX FIFO for TX channel n. (RO)

AHB_DMA_OUT_REMAIN_UNDER_1B_CHn Reserved. (RO)

AHB_DMA_OUT_REMAIN_UNDER_2B_CHn Reserved. (RO)

AHB_DMA_OUT_REMAIN_UNDER_3B_CHn Reserved. (RO)

AHB_DMA_OUT_REMAIN_UNDER_4B_CHn Reserved. (RO)
```