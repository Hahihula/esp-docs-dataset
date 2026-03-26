

```markdown
Register 43.18. SPI_DMA_INT_CLR_REG (0x0038)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) |
|     |    | SPI_APPI_INT_CLR<br>SPI_APPI2_INT_CLR<br>SPI_MST_TX_AFIFO_ERR_INT_CLR<br>SPI_MST_RX_AFIFO_ERR_INT_CLR<br>SPI_SLV_CMD_ERR_INT_CLR<br>SPI_SLV_BUF_ERR_INT_CLR<br>SPI_DMA_DONE_ERR_INT_CLR<br>SPI_SLV_WR_DONE_ERR_INT_CLR<br>SPI_SLV_RD_DONE_ERR_INT_CLR<br>SPI_SLV_WR_BUF_DONE_ERR_INT_CLR<br>SPI_SLV_RD_BUF_DONE_ERR_INT_CLR<br>SPI_TRANS_DONE_ERR_INT_CLR |
| Reset | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |    |

SPI_DMA_INFIFO_FULL_ERR_INT_CLR Write 1 to clear SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR Write 1 to clear SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)

SPI_SLV_EX_QPI_INT_CLR Write 1 to clear SPI_SLV_EX_QPI_INT interrupt. (WT)

SPI_SLV_EN_QPI_INT_CLR Write 1 to clear SPI_SLV_EN_QPI_INT interrupt. (WT)

SPI_SLV_CMD7_INT_CLR Write 1 to clear SPI_SLV_CMD7_INT interrupt. (WT)

SPI_SLV_CMD8_INT_CLR Write 1 to clear SPI_SLV_CMD8_INT interrupt. (WT)

SPI_SLV_CMD9_INT_CLR Write 1 to clear SPI_SLV_CMD9_INT interrupt. (WT)

SPI_SLV_CMDA_INT_CLR Write 1 to clear SPI_SLV_CMDA_INT interrupt. (WT)

SPI_SLV_RD_DMA_DONE_INT_CLR Write 1 to clear SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)

SPI_SLV_WR_DMA_DONE_INT_CLR Write 1 to clear SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)

SPI_SLV_RD_BUF_DONE_INT_CLR Write 1 to clear SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)

SPI_SLV_WR_BUF_DONE_INT_CLR Write 1 to clear SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)

SPI_TRANS_DONE_INT_CLR Write 1 to clear SPI_TRANS_DONE_INT interrupt. (WT)

Continued on the next page...
```