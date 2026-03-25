
```markdown
Register 29.17. SPI_DMA_INT_ENA_REG (0x0034)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | SPI_APPL_INT_ENA | SPI_APP2_INT_ENA | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ENA | SPI_MST_RX_AFIFO_FULL_ERR_INT_ENA | (reserved) | SPI_SEG_MAGIC_ERR_INT_ENA | SPI_DMA_SEG_TRANS_DONE_INT_ENA | SPI_SLV_WR_BUF_DONE_INT_ENA | SPI_SLV_RD_BUF_DONE_INT_ENA | SPI_SLV_WR_DMA_DONE_INT_ENA | SPI_SLV_RD_DMA_DONE_INT_ENA | SPI_SLV_CMD9_INT_ENA | SPI_SLV_CMD8_INT_ENA | SPI_SLV_CMD7_INT_ENA | SPI_SLV_EX_QPI_INT_ENA | SPI_SLV_EN_QPI_INT_ENA | SPI_SLV_CMD_INT_ENA | (reserved) |
|     |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

SPI_DMA_INFIFO_FULL_ERR_INT_ENA  Write 1 to enable SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (R/W)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ENA  Write 1 to enable SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (R/W)

SPI_SLV_EX_QPI_INT_ENA  Write 1 to enable SPI_SLV_EX_QPI_INT interrupt. (R/W)

SPI_SLV_EN_QPI_INT_ENA  Write 1 to enable SPI_SLV_EN_QPI_INT interrupt. (R/W)

SPI_SLV_CMD7_INT_ENA  Write 1 to enable SPI_SLV_CMD7_INT interrupt. (R/W)

SPI_SLV_CMD8_INT_ENA  Write 1 to enable SPI_SLV_CMD8_INT interrupt. (R/W)

SPI_SLV_CMD9_INT_ENA  Write 1 to enable SPI_SLV_CMD9_INT interrupt. (R/W)

SPI_SLV_CMD_INT_ENA  Write 1 to enable SPI_SLV_CMD_INT interrupt. (R/W)

SPI_SLV_RD_DMA_DONE_INT_ENA  Write 1 to enable SPI_SLV_RD_DMA_DONE_INT interrupt. (R/W)

SPI_SLV_WR_DMA_DONE_INT_ENA  Write 1 to enable SPI_SLV_WR_DMA_DONE_INT interrupt. (R/W)

SPI_SLV_RD_BUF_DONE_INT_ENA  Write 1 to enable SPI_SLV_RD_BUF_DONE_INT interrupt. (R/W)

SPI_SLV_WR_BUF_DONE_INT_ENA  Write 1 to enable SPI_SLV_WR_BUF_DONE_INT interrupt. (R/W)

SPI_TRANS_DONE_INT_ENA  Write 1 to enable SPI_TRANS_DONE_INT interrupt. (R/W)

SPI_DMA_SEG_TRANS_DONE_INT_ENA  Write 1 to enable SPI_DMA_SEG_TRANS_DONE_INT interrupt. (R/W)

SPI_SEG_MAGIC_ERR_INT_ENA  Write 1 to enable SPI_SEG_MAGIC_ERR_INT interrupt. (R/W)

SPI_SLV_CMD_ERR_INT_ENA  Write 1 to enable SPI_SLV_CMD_ERR_INT interrupt. (R/W)

SPI_MST_RX_AFIFO_WFULL_ERR_INT_ENA  Write 1 to enable SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt. (R/W)
```