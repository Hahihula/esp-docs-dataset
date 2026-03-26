

```markdown
Register 6.60. DMA2D_AXI_ERR_REG (0x0A00)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    | (reserved) | DMA2D_WR_BAK_FIFO_CNT | DMA2D_WR_FIFO_CNT | DMA2D_RD_BAK_FIFO_CNT | DMA2D_RD_FIFO_CNT | DMA2D_RRESP_ERR_CNT | DMA2D_WRESP_ERR_CNT | DMA2D_RD_ERR_CNT | Reset |
| Value | 0 | 0 | 0 | 0 | 0x0 | 0xD | 0xD | 0xD | 0xD | 0xD | 0xD | 0xD | 0xD |

DMA2D_RD_ERR_CNT Represents the number of AXI read ID errors. (RO)
DMA2D_RRESP_ERR_CNT Represents the number of AXI read response errors. (RO)
DMA2D_WRESP_ERR_CNT Represents the number of AXI write response errors. (RO)
DMA2D_RD_FIFO_CNT Represents the number of remaining commands in the AXI read command FIFO. (RO)
DMA2D_RD_BAK_FIFO_CNT Represents the number of remaining commands in the AXI read backup command FIFO. (RO)
DMA2D_WR_FIFO_CNT Represents the number of remaining commands in the AXI write command FIFO. (RO)
DMA2D_WR_BAK_FIFO_CNT Represents the number of remaining commands in the AXI write backup command FIFO. (RO)

Register 6.61. DMA2D_DATE_REG (0x0A2C)

| Bit | 31 | 30 | 29 | ... | 2 | 1 | 0 |
|-----|----|----|----|-----|---|---|---|
|     |    |    |    | DMA2D_DATE | Reset |
| Value | 0x2412190 |

DMA2D_DATE Version control register. (R/W)
```