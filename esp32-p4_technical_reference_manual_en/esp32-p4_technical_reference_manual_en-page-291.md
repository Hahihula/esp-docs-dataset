

```markdown
Register 4.52. AHB_DMA_IN_DSCR_BF1_CHn_REG (n: 0-2) (0x0098+0xC0*n)

AHB_DMA_INLINK_DSCR_BF1_CHn Represents the address of the previous receive descriptor x-1 that is pre-read. (RO)


Register 4.53. AHB_DMA_OUTFIFO_STATUS_CHn_REG (n: 0-2) (0x00D8+0xC0*n)

AHB_DMA_OUTFIFO_FULL_CHn Represents whether L1 TX FIFO is full.
O: Not Full
1: Full
(RO)

AHB_DMA_OUTFIFO_EMPTY_CHn Represents whether L1 TX FIFO is empty.
O: Not empty
1: Empty
(RO)

AHB_DMA_OUTFIFO_CNT_CHn Represents the number of data bytes in L1 TX FIFO for TX channel n. (RO)

AHB_DMA_OUT_REMAIN_UNDER_1B_CHn Reserved. (RO)
AHB_DMA_OUT_REMAIN_UNDER_2B_CHn Reserved. (RO)
AHB_DMA_OUT_REMAIN_UNDER_3B_CHn Reserved. (RO)
AHB_DMA_OUT_REMAIN_UNDER_4B_CHn Reserved. (RO)
```