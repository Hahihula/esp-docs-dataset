
```markdown
Register 27.20. SPI_DMA_INT_ST_REG (0x0040)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | SPI_APP1_INT_ST                        | The status bit for SPI_APP1_INT interrupt. (RO)                             |
| 29  | SPI_APP2_INT_ST                        | The status bit for SPI_APP2_INT interrupt. (RO)                             |
| 28  | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ST     | The status bit for SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt. (RO)           |
| 27  | SPI_MST_RX_AFIFO_WFULL_ERR_INT_ST      | The status bit for SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt. (RO)            |
| 26  | (reserved)                             |                                                                             |
| 25  | SPI_SLV_CMD_ERR_INT_ST                 | The status bit for SPI_SLV_CMD_ERR_INT interrupt. (RO)                      |
| 24  | SPI_SEG_MAGIC_ERR_INT_ST               | The status bit for SPI_SEG_MAGIC_ERR_INT interrupt. (RO)                    |
| 23  | SPI_DMA_SEGS_DONE_INT_ST               | The status bit for SPI_DMA_SEGS_DONE_INT interrupt. (RO)                    |
| 22  | SPI_SLV_WR_BUF_DONE_INT_ST             | The status bit for SPI_SLV_WR_BUF_DONE_INT interrupt. (RO)                  |
| 21  | SPI_SLV_RD_BUF_DONE_INT_ST             | The status bit for SPI_SLV_RD_BUF_DONE_INT interrupt. (RO)                  |
| 20  | SPI_SLV_CMD7_INT_ST                    | The status bit for SPI_SLV_CMD7_INT interrupt. (RO)                         |
| 19  | SPI_SLV_CMD8_INT_ST                    | The status bit for SPI_SLV_CMD8_INT interrupt. (RO)                         |
| 18  | SPI_SLV_CMD9_INT_ST                    | The status bit for SPI_SLV_CMD9_INT interrupt. (RO)                         |
| 17  | SPI_SLV_CMDA_INT_ST                    | The status bit for SPI_SLV_CMDA_INT interrupt. (RO)                         |
| 16  | SPI_SLV_RD_DMA_DONE_INT_ST             | The status bit for SPI_SLV_RD_DMA_DONE_INT interrupt. (RO)                  |
| 15  | SPI_SLV_WR_DMA_DONE_INT_ST             | The status bit for SPI_SLV_WR_DMA_DONE_INT interrupt. (RO)                  |
| 14  | SPI_SLV_EX_QPI_INT_ST                  | The status bit for SPI_SLV_EX_QPI_INT interrupt. (RO)                       |
| 13  | SPI_SLV_EN_QPI_INT_ST                  | The status bit for SPI_SLV_EN_QPI_INT interrupt. (RO)                       |
| 12  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ST       | The status bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (RO)            |
| 11  | SPI_DMA_INFIFO_FULL_ERR_INT_ST         | The status bit for SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (RO)              |
| 10  | SPI_SLV_CMD7_INT_ST                    | The status bit for SPI_SLV_CMD7_INT interrupt. (RO)                         |
| 9   | SPI_SLV_CMD8_INT_ST                    | The status bit for SPI_SLV_CMD8_INT interrupt. (RO)                         |
| 8   | SPI_SLV_CMD9_INT_ST                    | The status bit for SPI_SLV_CMD9_INT interrupt. (RO)                         |
| 7   | SPI_SLV_CMDA_INT_ST                    | The status bit for SPI_SLV_CMDA_INT interrupt. (RO)                         |
| 6   | SPI_SLV_RD_DMA_DONE_INT_ST             | The status bit for SPI_SLV_RD_DMA_DONE_INT interrupt. (RO)                  |
| 5   | SPI_SLV_WR_DMA_DONE_INT_ST             | The status bit for SPI_SLV_WR_DMA_DONE_INT interrupt. (RO)                  |
| 4   | SPI_SLV_EX_QPI_INT_ST                  | The status bit for SPI_SLV_EX_QPI_INT interrupt. (RO)                       |
| 3   | SPI_SLV_EN_QPI_INT_ST                  | The status bit for SPI_SLV_EN_QPI_INT interrupt. (RO)                       |
| 2   | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ST       | The status bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (RO)            |
| 1   | SPI_DMA_INFIFO_FULL_ERR_INT_ST         | The status bit for SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (RO)              |
| 0   | Reset                                  |                                                                             |

SPI_DMA_INFIFO_FULL_ERR_INT_ST    The status bit for SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (RO)
SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ST   The status bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (RO)
SPI_SLV_EX_QPI_INT_ST              The status bit for SPI_SLV_EX_QPI_INT interrupt. (RO)
SPI_SLV_EN_QPI_INT_ST              The status bit for SPI_SLV_EN_QPI_INT interrupt. (RO)
SPI_SLV_CMD7_INT_ST                The status bit for SPI_SLV_CMD7_INT interrupt. (RO)
SPI_SLV_CMD8_INT_ST                The status bit for SPI_SLV_CMD8_INT interrupt. (RO)
SPI_SLV_CMD9_INT_ST                The status bit for SPI_SLV_CMD9_INT interrupt. (RO)
SPI_SLV_CMDA_INT_ST                The status bit for SPI_SLV_CMDA_INT interrupt. (RO)
SPI_SLV_RD_DMA_DONE_INT_ST         The status bit for SPI_SLV_RD_DMA_DONE_INT interrupt. (RO)
SPI_SLV_WR_DMA_DONE_INT_ST         The status bit for SPI_SLV_WR_DMA_DONE_INT interrupt. (RO)
SPI_SLV_RD_BUF_DONE_INT_ST         The status bit for SPI_SLV_RD_BUF_DONE_INT interrupt. (RO)
SPI_SLV_WR_BUF_DONE_INT_ST         The status bit for SPI_SLV_WR_BUF_DONE_INT interrupt. (RO)
SPI_TRANS_DONE_INT_ST              The status bit for SPI_TRANS_DONE_INT interrupt. (RO)
SPI_DMA_SEG_TRANS_DONE_INT_ST      The status bit for SPI_DMA_SEG_TRANS_DONE_INT interrupt. (RO)
SPI_SEG_MAGIC_ERR_INT_ST           The status bit for SPI_SEG_MAGIC_ERR_INT interrupt. (RO)
SPI_SLV_CMD_ERR_INT_ST             The status bit for SPI_SLV_CMD_ERR_INT interrupt. (RO)

Continued on the next page...
```