

```markdown
Register 3.20. GDMA_INFIFO_STATUS_CHn_REG (n: 0-2) (0x0078+0xC0*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 0  | (reserved) | GDMA_IN_BUF_HUNGRY_CHn | GDMA_IN_REMAIN_UNDER_4B_CHn | GDMA_IN_REMAIN_UNDER_3B_CHn | GDMA_IN_REMAIN_UNDER_2B_CHn | GDMA_IN_REMAIN_UNDER_1B_CHn | GDMA_INFIFO_CNT_CHn | GDMA_INFIFO_EMPTY_CHn | GDMA_INFIFO_FULL_CHn |
| Description | (reserved) | (reserved) | (reserved) | (reserved) | GDMA_INFIFO_FULL_CHn | Represents whether or not L1 RX FIFO is full. <br> O: Not Full <br> 1: Full <br> (RO) | GDMA_INFIFO_EMPTY_CHn | Represents whether or not L1 RX FIFO is empty. <br> O: Not empty <br> 1: Empty <br> (RO) | GDMA_INFIFO_CNT_CHn | Represents the number of data bytes in L1 RX FIFO for RX channel n. (RO) | GDMA_IN_REMAIN_UNDER_1B_CHn | Reserved. (RO) | GDMA_IN_REMAIN_UNDER_2B_CHn | Reserved. (RO) | GDMA_IN_REMAIN_UNDER_3B_CHn | Reserved. (RO) | GDMA_IN_REMAIN_UNDER_4B_CHn | Reserved. (RO) | GDMA_IN_BUF_HUNGRY_CHn | Reserved. (RO) |
```