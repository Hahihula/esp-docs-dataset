

```markdown
Register 2.15. GDMA_INFIFO_STATUS_CHn_REG (n: 0-2) (0x0078+192*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | GDMA_IN_BUF_HUNGRY_CHn                                                     |
| 29  | GDMA_IN_REMAIN_UNDER_4B_CHn                                                |
| 28  | GDMA_IN_REMAIN_UNDER_3B_CHn                                                |
| 27  | GDMA_IN_REMAIN_UNDER_2B_CHn                                                |
| 26  | GDMA_IN_REMAIN_UNDER_1B_CHn                                                |
| 25  | (reserved)                                                                  |
| 24  | GDMA_INFIFO_FULL_CHn L1 RX FIFO full signal for RX channel O. (RO)         |
| 23  | GDMA_INFIFO_EMPTY_CHn L1 RX FIFO empty signal for RX channel O. (RO)       |
| 22  | GDMA_INFIFO_CNT_CHn The register stores the byte number of the data in L1 RX FIFO for RX channel O. (RO) |
| 21  | GDMA_IN_REMAIN_UNDER_1B_CHn Reserved. (RO)                                 |
| 20  | GDMA_IN_REMAIN_UNDER_2B_CHn Reserved. (RO)                                 |
| 19  | GDMA_IN_REMAIN_UNDER_3B_CHn Reserved. (RO)                                 |
| 18  | GDMA_IN_REMAIN_UNDER_4B_CHn Reserved. (RO)                                 |
| 17  | GDMA_IN_BUF_HUNGRY_CHn Reserved. (RO)                                      |

Register 2.16. GDMA_IN_STATE_CHn_REG (n: 0-2) (0x0084+192*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | GDMA_INLINK_DSCR_ADDR_CHn This register stores the lower 18 bits of the next receive descriptor address that is pre-read (but not processed yet). If the current receive descriptor is the last descriptor, then this field represents the address of the current receive descriptor. (RO) |
| 29  | GDMA_IN_DSCR_STATE_CHn Reserved. (RO)                                      |
| 28  | GDMA_IN_STATE_CHn Reserved. (RO)                                           |
```