

```markdown
Register 6.47. DMA2D_OUTFIFO_STATUS_CHn_REG (n: 0-3) (0x0014+0x100*n)

Continued from the previous page...

DMA2D_OUTFIFO_FULL_L3_CHn Represents whether the L3 TX FIFO for TX channel n is full.
O: Not full
1: Full
(RO)

DMA2D_OUTFIFO_EMPTY_L3_CHn Represents whether the L3 TX FIFO for TX channel n is empty.
O: Not empty
1: Empty
(RO)

DMA2D_OUTFIFO_CNT_L3_CHn Represents the number of data bytes in L3 TX FIFO for TX channel n. (RO)


Register 6.48. DMA2D_OUT_STATE_CHn_REG (n: 0-3) (0x0024+0x100*n)
```
```markdown
DMA2D_OUTLINK_DSCR_ADDR_CHn Represents the lower 18 bits of the next transmit descriptor address that is pre-read (but not processed yet). If the current transmit descriptor is the last descriptor, then this field represents the address of the current transmit descriptor. (RO)

DMA2D_OUT_RESET_AVAIL_CHn Represents whether it is safe to reset TX channel n.
O: Not safe
1: Safe
(RO)
```