

```markdown
Register 33.18. SPI_DMA_INT_CLR_REG (0x0038)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | SPI_APPI_INT_CLR                |                                                                             |
| 29  | SPI_MST_TX_AFIFO_ERR_INT_CLR   |                                                                             |
| 28  | SPI_MST_RX_AFIFO_ERR_INT_CLR   |                                                                             |
| 27  | SPI_SLV_CMD_ERR_INT_CLR        |                                                                             |
| 26  | SPI_DMA_OUTFIFO_ERR_INT_CLR    |                                                                             |
| 25  | SPI_SLV_BUF_ERR_INT_CLR        |                                                                             |
| 24  | MAGIC_TRNG_DONE_INT_CLR        |                                                                             |
| 23  | SPI_SLV_RDRDY_DONE_INT_CLR     |                                                                             |
| 22  | SPI_SLV_WRDY_DONE_INT_CLR      |                                                                             |
| 21  | SPI_DMA_DONE_INT_CLR           |                                                                             |
| 20  | SPI_CMD8_DONE_INT_CLR          |                                                                             |
| 19  | SPI_CMD9_DONE_INT_CLR          |                                                                             |
| 18  | SPI_CMD_EN_OP_INT_CLR          |                                                                             |
| 17  | SPI_DMA_INFO_OUTFIFO_EMPTY_ERR_INT_CLR |                                     |
| 16  | SPI_DMA_INFFIFO_FULL_ERR_INT_CLR |                                     |
| 15  | SPI_SLV_EX_QPI_INT_CLR         |                                     |
| 14  | SPI_SLV_EN_QPI_INT_CLR         |                                     |
| 13  | SPI_SLV_CMD7_INT_CLR           |                                     |
| 12  | SPI_SLV_CMD8_INT_CLR           |                                     |
| 11  | SPI_SLV_CMD9_INT_CLR           |                                     |
| 10  | SPI_SLV_CMDA_INT_CLR           |                                     |
| 9   | SPI_SLV_RD_DMA_DONE_INT_CLR    |                                     |
| 8   | SPI_SLV_WR_DMA_DONE_INT_CLR    |                                     |
| 7   | SPI_SLV_RD_BUF_DONE_INT_CLR    |                                     |
| 6   | SPI_SLV_WR_BUF_DONE_INT_CLR    |                                     |

SPI_DMA_INFIFO_FULL_ERR_INT_CLR Write 1 to clear the SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)
SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR Write 1 to clear the SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)
SPI_SLV_EX_QPI_INT_CLR Write 1 to clear the SPI_SLV_EX_QPI_INT interrupt. (WT)
SPI_SLV_EN_QPI_INT_CLR Write 1 to clear the SPI_SLV_EN_QPI_INT interrupt. (WT)
SPI_SLV_CMD7_INT_CLR Write 1 to clear the SPI_SLV_CMD7_INT interrupt. (WT)
SPI_SLV_CMD8_INT_CLR Write 1 to clear the SPI_SLV_CMD8_INT interrupt. (WT)
SPI_SLV_CMD9_INT_CLR Write 1 to clear the SPI_SLV_CMD9_INT interrupt. (WT)
SPI_SLV_CMDA_INT_CLR Write 1 to clear the SPI_SLV_CMDA_INT interrupt. (WT)
SPI_SLV_RD_DMA_DONE_INT_CLR Write 1 to clear the SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)
SPI_SLV_WR_DMA_DONE_INT_CLR Write 1 to clear the SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)
SPI_SLV_RD_BUF_DONE_INT_CLR Write 1 to clear the SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)
SPI_SLV_WR_BUF_DONE_INT_CLR Write 1 to clear the SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)

Continued on the next page...
```