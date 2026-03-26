

```markdown
Register 6.17. DMA2D_IN_CONFO_CHn_REG (n: 0-2) (0x0500+0x100*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | DMA2D_IN_ARB_WEIGHT_OPT_DIS_CHn            | Configures whether to disable the arbitration weight optimization for RX channel n. |
| 29  | DMA2D_IN_CMD_DISABLE_CHn                   |                                                                             |
| 28  | DMA2D_IN_CMD_RST_CHn                       |                                                                             |
| 27  | (reserved)                                 |                                                                             |
| 26  | DMA2D_IN_REORDER_EN_CHO                    | Configures whether to enable reorder for RX channel n.                      |
| 25  | DMA2D_IN_DSCR_PORT_EN_CHn                  | Enables descriptor port access for RX channel n.                             |
| 24  | DMA2D_IN_DSCR_PORT_EN_CHn                  |                                                                             |
| 23  | (reserved)                                 |                                                                             |
| 22  | DMA2D_IN_ECC_AES_EN_CHn                    | Configures whether to enable the access to external memory space for ECC and AES via RX channel n. |
| 21  | DMA2D_IN_CHECK_OWNER_CHn                   | Configures whether to enable the owner bit check for RX channel n.           |
| 20  | (reserved)                                 |                                                                             |
| 19  | DMA2D_IN_INDSCR_BURST_EN_CHn               | Enables INCR burst transfer access descriptors when accessing internal memory via RX channel n. |
| 18  | DMA2D_IN_MEM_BURST_LENGTH_CHn              | Configures the burst length for RX channel n:                              |
|     |                                             | 0: 8 bytes                                                                   |
|     |                                             | 1: 16 bytes                                                                  |
|     |                                             | 2: 32 bytes                                                                  |
|     |                                             | 3: 64 bytes                                                                  |
|     |                                             | 4: 128 bytes                                                                 |
|     | Others: Invalid                             |                                                                             |
| 17  | (reserved)                                 |                                                                             |
| 16  | DMA2D_IN_MEM_TRANS_EN_CHn                  | Configures whether to enable memory-to-memory data transfer for TX and RX channel n. |
| 15  |                                             | O: Disable                                                                   |
|     |                                             | 1: Enable                                                                    |
| 14  | (reserved)                                 |                                                                             |
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

DMA2D_IN_MEM_TRANS_EN_CHn Configures whether to enable memory-to-memory data transfer for TX and RX channel n.
O: Disable
1: Enable
(R/W)

DMA2D_IN_DSCR_BURST_EN_CHn Configures whether to enable INCR burst transfer for RX channel n to read descriptors when accessing internal memory.
O: Disable
1: Enable
(R/W)

DMA2D_IN_ECC_AES_EN_CHn Configures whether to enable the access to external memory space for ECC and AES (encrypted) via RX channel n.
O: Disable
1: Enable. In this case, the starting address of the space and the corresponding data should be 16-byte aligned.
(R/W)

DMA2D_IN_CHECK_OWNER_CHn Configures whether to enable the owner bit check for RX channel n.
O: Disable
1: Enable
(R/W)

DMA2D_IN_MEM_BURST_LENGTH_CHn Configures the burst length for RX channel n.
0: 8 bytes
1: 16 bytes
2: 32 bytes
3: 64 bytes
4: 128 bytes
Others: Invalid
(R/W)

Continued on the next page...
```