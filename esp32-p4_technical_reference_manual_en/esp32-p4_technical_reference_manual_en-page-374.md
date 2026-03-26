

```markdown
Register 5.11. DMAC_CHn_CTLO_REG (n: 1-4) (0x0100*n + 0x0018)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | DMAC_CHn_NONPOSTED_LASTWRITE_EN            | (reserved)                                                                  |
| 29  |                                             |                                                                             |
| 28  |                                             |                                                                             |
| 27  |                                             |                                                                             |
| 26  |                                             |                                                                             |
| 25  |                                             |                                                                             |
| 24  | DMAC_CHn_DST_MSZE                          | (reserved)                                                                  |
| 23  | DMAC_CHn_DST_TR_WIDTH                      | (reserved)                                                                  |
| 22  | DMAC_CHn_SRC_MSZE                          | (reserved)                                                                  |
| 21  | DMAC_CHn_DINC                              | (reserved)                                                                  |
| 20  | DMAC_CHn_SINC                              | (reserved)                                                                  |
| 19  | DMAC_CHn_DMS                               | (reserved)                                                                  |
| 18  | DMAC_CHn_SMS                               |                                                                             |
| 17  |                                             |                                                                             |
| 16  |                                             |                                                                             |
| 15  |                                             |                                                                             |
| 14  |                                             |                                                                             |
| 13  |                                             |                                                                             |
| 12  |                                             |                                                                             |
| 11  |                                             |                                                                             |
| 10  |                                             |                                                                             |
| 9   |                                             |                                                                             |
| 8   |                                             |                                                                             |
| 7   |                                             |                                                                             |
| 6   |                                             |                                                                             |
| 5   |                                             |                                                                             |
| 4   |                                             |                                                                             |
| 3   |                                             |                                                                             |
| 2   |                                             |                                                                             |
| 1   |                                             |                                                                             |
| 0   | Reset                                      | 0x0                                                                          |

DMAC_CHn_SMS Configures which AXI master to access the source.
O: AXI Master 1
1: AXI Master 2
(R/W)

DMAC_CHn_DMS Configures which AXI master to access the destination.
O: AXI Master 1
1: AXI Master 2
(R/W)

DMAC_CHn_SINC Configures whether to increment the source address on every source transfer.
If VDMA is fetching data from a source peripheral's FIFO at a fixed address, then set this field to 1.
O: Increment
1: No change
(R/W)

DMAC_CHn_DINC Configures whether to increment the destination address on every destination transfer.
If VDMA is writing data to a source peripheral's FIFO at a fixed address, then set this field to 1.
O: Increment
1: No change
(R/W)

DMAC_CHn_SRC_TR_WIDTH Configures source transfer width.
0x0: 8 bits
0x1: 16 bits
0x2: 32 bits
0x3: 64 bits
(R/W)
```
Continued on the next page...
```