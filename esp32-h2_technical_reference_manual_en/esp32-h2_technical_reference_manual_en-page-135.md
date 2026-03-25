

```markdown
Register 3.26. GDMA_IN_DSCR_BF1_CHn_REG (n: 0-2) (0x0098+0xC0*n)

GDMA_INLINK_DSCR_BF1_CHn Represents the address of the previous receive descriptor x-1 that is pre-read. (RO)


Register 3.27. GDMA_OUTFIFO_STATUS_CHn_REG (n: 0-2) (0x00D8+0xC0*n)

GDMA_OUTFIFO_FULL_CHn Represents whether or not L1 TX FIFO is full.
O: Not Full
1: Full
(RO)

GDMA_OUTFIFO_EMPTY_CHn Represents whether or not L1 TX FIFO is empty.
O: Not empty
1: Empty
(RO)

GDMA_OUTFIFO_CNT_CHn Represents the number of data bytes in L1 TX FIFO for TX channel n. (RO)

GDMA_OUT_REMAIN_UNDER_1B_CHn Reserved. (RO)
GDMA_OUT_REMAIN_UNDER_2B_CHn Reserved. (RO)
GDMA_OUT_REMAIN_UNDER_3B_CHn Reserved. (RO)
GDMA_OUT_REMAIN_UNDER_4B_CHn Reserved. (RO)
```