

```markdown
Register 33.17. SPI_DMA_INT_ENA_REG (0x0034)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |
|     | SPI_APPL_INT_ENA      | SPI_APP2_INT_ENA       | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ENA | SPI_MST_RX_AFIFO_FULL_ERR_INT_ENA | SPI_SLV_CMD_ERR_INT_ENA | SPI_SLV_BUF_ERR_INT_ENA | SPI_DMA_SEG_ERR_INT_ENA | SPI_DMA_MAGIC_ERR_INT_ENA | SPI_DMA_TRANS_DONE_INT_ENA | SPI_SLV_WR_DONE_INT_ENA | SPI_SLV_RD_DONE_INT_ENA | SPI_SLV_CMD8_INT_ENA | SPI_SLV_CMD9_INT_ENA | SPI_SLV_EX_QPI_INT_ENA | SPI_SLV_EN_QPI_INT_ENA | SPI_SLV_CMD7_INT_ENA | SPI_DMA_INFIFO_FULL_ERR_INT_ENA | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ENA |
```

SPI_DMA_INFIFO_FULL_ERR_INT_ENA Write 1 to enable the SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (R/W)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ENA Write 1 to enable the SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (R/W)

SPI_SLV_EX_QPI_INT_ENA Write 1 to enable the SPI_SLV_EX_QPI_INT interrupt. (R/W)

SPI_SLV_EN_QPI_INT_ENA Write 1 to enable the SPI_SLV_EN_QPI_INT interrupt. (R/W)

SPI_SLV_CMD7_INT_ENA Write 1 to enable the SPI_SLV_CMD7_INT interrupt. (R/W)

SPI_SLV_CMD8_INT_ENA Write 1 to enable the SPI_SLV_CMD8_INT interrupt. (R/W)

SPI_SLV_CMD9_INT_ENA Write 1 to enable the SPI_SLV_CMD9_INT interrupt. (R/W)

SPI_SLV_CMDA_INT_ENA Write 1 to enable the SPI_SLV_CMDA_INT interrupt. (R/W)

SPI_SLV_RD_DMA_DONE_INT_ENA Write 1 to enable the SPI_SLV_RD_DMA_DONE_INT interrupt. (R/W)

SPI_SLV_WR_DMA_DONE_INT_ENA Write 1 to enable the SPI_SLV_WR_DMA_DONE_INT interrupt. (R/W)

SPI_SLV_RD_BUF_DONE_INT_ENA Write 1 to enable the SPI_SLV_RD_BUF_DONE_INT interrupt. (R/W)

SPI_SLV_WR_BUF_DONE_INT_ENA Write 1 to enable the SPI_SLV_WR_BUF_DONE_INT interrupt. (R/W)

Continued on the next page...
```