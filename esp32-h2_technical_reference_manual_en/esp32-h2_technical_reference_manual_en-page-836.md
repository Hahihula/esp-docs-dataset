
```markdown
Register 29.21. SPI_DMA_INT_SET_REG (0x0044)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | SPI_APPI_INT_SET                           | Write 1 to set SPI_APPI_INT interrupt. (WT)                                |
| 29  | SPI_APP2_INT_SET                           | Write 1 to set SPI_APP2_INT interrupt. (WT)                                |
| 28  | SPI_MST_TX_INT_SET                         | Write 1 to set SPI_MST_TX_INT interrupt. (WT)                              |
| 27  | SPI_MST_RX_AFIFO_REMPTY_ERR_INT_SET        | Write 1 to set SPI_MST_RX_AFIFO_REMPTY_ERR_INT interrupt. (WT)              |
| 26  | SPI_SIV_CMD_ERR_INT_SET                    | Write 1 to set SPI_SIV_CMD_ERR_INT interrupt. (WT)                         |
| 25  | (reserved)                                 |                                                                             |
| 24  | SPI_SEG_MAGIC_ERR_INT_SET                  | Write 1 to set SPI_SEG_MAGIC_ERR_INT interrupt. (WT)                       |
| 23  | SPI_DMA_SEG_TRANSDONE_INT_SET              | Write 1 to set SPI_DMA_SEG_TRANSDONE_INT interrupt. (WT)                   |
| 22  | SPI_SLV_WR_BUF_DONE_INT_SET                | Write 1 to set SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)                     |
| 21  | SPI_SLV_RD_BUF_DONE_INT_SET                | Write 1 to set SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)                     |
| 20  | SPI_SLV_WR_DMA_DONE_INT_SET                | Write 1 to set SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)                     |
| 19  | SPI_SLV_RD_DMA_DONE_INT_SET                | Write 1 to set SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)                     |
| 18  | SPI_SLV_CMDA_INT_SET                       | Write 1 to set SPI_SLV_CMDA_INT interrupt. (WT)                            |
| 17  | SPI_SLV_CMD9_INT_SET                       | Write 1 to set SPI_SLV_CMD9_INT interrupt. (WT)                            |
| 16  | SPI_SLV_CMD8_INT_SET                       | Write 1 to set SPI_SLV_CMD8_INT interrupt. (WT)                            |
| 15  | SPI_SLV_CMD7_INT_SET                       | Write 1 to set SPI_SLV_CMD7_INT interrupt. (WT)                            |
| 14  | SPI_SLV_EN_QPI_INT_SET                     | Write 1 to set SPI_SLV_EN_QPI_INT interrupt. (WT)                          |
| 13  | SPI_SLV_EX_QPI_INT_SET                     | Write 1 to set SPI_SLV_EX_QPI_INT interrupt. (WT)                          |
| 12  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET          | Write 1 to set SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)               |
| 11  | SPI_DMA_INFIFO_FULL_ERR_INT_SET            | Write 1 to set SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)                 |
| 10-7| (reserved)                                 |                                                                             |
| 6   | SPI_SIV_CMD9_INT_SET                       | Write 1 to set SPI_SIV_CMD9_INT interrupt. (WT)                            |
| 5   | SPI_SIV_CMD8_INT_SET                       | Write 1 to set SPI_SIV_CMD8_INT interrupt. (WT)                            |
| 4   | SPI_SIV_CMD7_INT_SET                       | Write 1 to set SPI_SIV_CMD7_INT interrupt. (WT)                            |
| 3   | SPI_SIV_CMD_EN_QPI_INT_SET                 | Write 1 to set SPI_SIV_CMD_EN_QPI_INT interrupt. (WT)                      |
| 2   | SPI_SLV_WR_BUF_DONE_INT_SET                | Write 1 to set SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)                     |
| 1   | SPI_SLV_RD_BUF_DONE_INT_SET                | Write 1 to set SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)                     |
| 0   | SPI_DMA_INFIFO_EMPTY_ERR_INT_SET           | Write 1 to set SPI_DMA_INFIFO_EMPTY_ERR_INT interrupt. (WT)                |

SPI_DMA_INFIFO_FULL_ERR_INT_SET    Write 1 to set SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)
SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET  Write 1 to set SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)
SPI_SLV_EX_QPI_INT_SET             Write 1 to set SPI_SLV_EX_QPI_INT interrupt. (WT)
SPI_SLV_EN_QPI_INT_SET             Write 1 to set SPI_SLV_EN_QPI_INT interrupt. (WT)
SPI_SLV_CMD7_INT_SET               Write 1 to set SPI_SLV_CMD7_INT interrupt. (WT)
SPI_SLV_CMD8_INT_SET               Write 1 to set SPI_SLV_CMD8_INT interrupt. (WT)
SPI_SLV_CMD9_INT_SET               Write 1 to set SPI_SLV_CMD9_INT interrupt. (WT)
SPI_SLV_CMDA_INT_SET               Write 1 to set SPI_SLV_CMDA_INT interrupt. (WT)
SPI_SLV_RD_DMA_DONE_INT_SET        Write 1 to set SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)
SPI_SLV_WR_DMA_DONE_INT_SET        Write 1 to set SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)
SPI_SLV_RD_BUF_DONE_INT_SET        Write 1 to set SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)
SPI_SLV_WR_BUF_DONE_INT_SET        Write 1 to set SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)
SPI_TRANS_DONE_INT_SET             Write 1 to set SPI_TRANS_DONE_INT interrupt. (WT)
SPI_DMA_SEG_TRANSDONE_INT_SET      Write 1 to set SPI_DMA_SEG_TRANSDONE_INT interrupt. (WT)
SPI_SEG_MAGIC_ERR_INT_SET          Write 1 to set SPI_SEG_MAGIC_ERR_INT interrupt. (WT)
SPI_SLV_CMD_ERR_INT_SET            Write 1 to set SPI_SLV_CMD_ERR_INT interrupt. (WT)

Continued on the next page...
```