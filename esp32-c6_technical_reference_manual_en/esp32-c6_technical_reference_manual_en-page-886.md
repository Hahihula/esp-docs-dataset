
```markdown
Register 28.18. SPI_DMA_INT_CLR_REG (0x0038)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | SPI_APP1_INT_CLR                          |                                                                             |
| 29  | SPI_APP2_INT_CLR                          |                                                                             |
| 28  | SPI_MST_TX_REMOPTY_ERR_INT_CLR            |                                                                             |
| 27  | SPI_MST_RX_AFULL_ERR_INT_CLR              |                                                                             |
| 26  | (reserved)                                |                                                                             |
| 25  | SPI_SEG_CMD_ERR_INT_CLR                   |                                                                             |
| 24  | SPI_DMA_SEG_TRANS_DONE_INT_CLR            |                                                                             |
| 23  | SPI_SLV_RBUF_DONE_INT_CLR                 |                                                                             |
| 22  | SPI_SLV_WR_BUF_DONE_INT_CLR               |                                                                             |
| 21  | SPI_SLV_CMD9_INT_CLR                      |                                                                             |
| 20  | SPI_SLV_CMD8_INT_CLR                      |                                                                             |
| 19  | SPI_SLV_CMD7_INT_CLR                      |                                                                             |
| 18  | SPI_SLV_EN_QPI_INT_CLR                    |                                                                             |
| 17  | SPI_SLV_EX_QPI_INT_CLR                    |                                                                             |
| 16  | (reserved)                                |                                                                             |
| 15  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR         | Write 1 to clear SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)             |
| 14  | SPI_DMA_INFIFO_FULL_ERR_INT_CLR           | Write 1 to clear SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)                |
| 13  | SPI_SLV_WR_DMA_DONE_INT_CLR               | Write 1 to clear SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)                    |
| 12  | SPI_SLV_RD_DMA_DONE_INT_CLR               | Write 1 to clear SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)                    |
| 11  | SPI_SLV_CMDA_INT_CLR                      | Write 1 to clear SPI_SLV_CMDA_INT interrupt. (WT)                           |
| 10  | SPI_SLV_CMD9_INT_CLR                      | Write 1 to clear SPI_SLV_CMD9_INT interrupt. (WT)                           |
| 9   | SPI_SLV_CMD8_INT_CLR                      | Write 1 to clear SPI_SLV_CMD8_INT interrupt. (WT)                           |
| 8   | SPI_SLV_CMD7_INT_CLR                      | Write 1 to clear SPI_SLV_CMD7_INT interrupt. (WT)                           |
| 7   | SPI_SLV_EN_QPI_INT_CLR                    | Write 1 to clear SPI_SLV_EN_QPI_INT interrupt. (WT)                         |
| 6   | SPI_SLV_EX_QPI_INT_CLR                    | Write 1 to clear SPI_SLV_EX_QPI_INT interrupt. (WT)                         |
| 5   | (reserved)                                |                                                                             |
| 4   | SPI_DMA_SEG_TRANS_DONE_INT_CLR            | Write 1 to clear SPI_DMA_SEG_TRANS_DONE_INT interrupt. (WT)                 |
| 3   | SPI_SLV_WR_BUF_DONE_INT_CLR               | Write 1 to clear SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)                    |
| 2   | SPI_SLV_RD_BUF_DONE_INT_CLR               | Write 1 to clear SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)                    |
| 1   | SPI_DMA_INFIFO_FULL_ERR_INT_CLR           | Write 1 to clear SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)                |
| 0   | Reset                                     |                                                                             |

SPI_DMA_INFIFO_FULL_ERR_INT_CLR    Write 1 to clear SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)
SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR  Write 1 to clear SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)
SPI_SLV_EX_QPI_INT_CLR             Write 1 to clear SPI_SLV_EX_QPI_INT interrupt. (WT)
SPI_SLV_EN_QPI_INT_CLR             Write 1 to clear SPI_SLV_EN_QPI_INT interrupt. (WT)
SPI_SLV_CMD7_INT_CLR               Write 1 to clear SPI_SLV_CMD7_INT interrupt. (WT)
SPI_SLV_CMD8_INT_CLR               Write 1 to clear SPI_SLV_CMD8_INT interrupt. (WT)
SPI_SLV_CMD9_INT_CLR               Write 1 to clear SPI_SLV_CMD9_INT interrupt. (WT)
SPI_SLV_CMDA_INT_CLR               Write 1 to clear SPI_SLV_CMDA_INT interrupt. (WT)
SPI_SLV_RD_DMA_DONE_INT_CLR        Write 1 to clear SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)
SPI_SLV_WR_DMA_DONE_INT_CLR        Write 1 to clear SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)
SPI_SLV_RD_BUF_DONE_INT_CLR        Write 1 to clear SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)
SPI_SLV_WR_BUF_DONE_INT_CLR        Write 1 to clear SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)
SPI_TRANS_DONE_INT_CLR             Write 1 to clear SPI_TRANS_DONE_INT interrupt. (WT)
SPI_DMA_SEG_TRANS_DONE_INT_CLR     Write 1 to clear SPI_DMA_SEG_TRANS_DONE_INT interrupt. (WT)
SPI_SEG_MAGIC_ERR_INT_CLR          Write 1 to clear SPI_SEG_MAGIC_ERR_INT interrupt. (WT)

Continued on the next page...
```