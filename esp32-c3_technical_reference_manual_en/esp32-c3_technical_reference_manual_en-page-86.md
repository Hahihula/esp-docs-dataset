

```markdown
Register 2.22. GDMA_OUTFIFO_STATUS_CHn_REG (n: 0-2) (0x00D8+192*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 27  | GDMA_OUT_REMAIN_UNDER_4B_CHn   |                                                                             |
| 26  | GDMA_OUT_REMAIN_UNDER_3B_CHn   |                                                                             |
| 25  | GDMA_OUT_REMAIN_UNDER_2B_CHn   |                                                                             |
| 24  | GDMA_OUT_REMAIN_UNDER_1B_CHn   |                                                                             |
| 23  | (reserved)                    |                                                                             |
| 22  | (reserved)                    |                                                                             |
| 8   | GDMA_OUTFIFO_CNT_CHn          |                                                                             |
| 7   | GDMA_OUTFIFO_EMPTY_CHn        |                                                                             |
| 2   | GDMA_OUTFIFO_FULL_CHn         | L1 TX FIFO full signal for TX channel O. (RO)                               |
| 1   |                                |                                                                             |
| 0   | Reset                         |                                                                             |

GDMA_OUTFIFO_FULL_CHn    L1 TX FIFO full signal for TX channel O. (RO)
GDMA_OUTFIFO_EMPTY_CHn   L1 TX FIFO empty signal for TX channel O. (RO)
GDMA_OUTFIFO_CNT_CHn     The register stores the byte number of the data in L1 TX FIFO for TX channel O. (RO)
GDMA_OUT_REMAIN_UNDER_1B_CHn Reserved. (RO)
GDMA_OUT_REMAIN_UNDER_2B_CHn Reserved. (RO)
GDMA_OUT_REMAIN_UNDER_3B_CHn Reserved. (RO)
GDMA_OUT_REMAIN_UNDER_4B_CHn Reserved. (RO)

Register 2.23. GDMA_OUT_STATE_CHn_REG (n: 0-2) (0x00E4+192*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 23  | GDMA_OUT_STATE_CHn            |                                                                             |
| 22  |                                |                                                                             |
| 20  | GDMA_OUTLINK_DSCR_ADDR_CHn    | This register stores the lower 18 bits of the next receive descriptor address that is pre-read (but not processed yet). If the current receive descriptor is the last descriptor, then this field represents the address of the current receive descriptor. (RO) |
| 19  |                                |                                                                             |
| 18  | GDMA_OUT_DSCR_STATE_CHn       | Reserved. (RO)                                                              |
| 17  | GDMA_OUT_STATE_CHn            | Reserved. (RO)                                                              |
```