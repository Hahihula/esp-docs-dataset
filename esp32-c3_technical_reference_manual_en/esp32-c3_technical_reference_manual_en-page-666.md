

```markdown
Register 2718. SPI_DMA_INT_CLR_REG (0x0038)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | SPI_APP1_INT_CLR                       | The clear bit for SPI_APP1_INT interrupt. (WT)                              |
| 29  | SPI_APP2_INT_CLR                       | The clear bit for SPI_APP2_INT interrupt. (WT)                              |
| 28  | SPI_MST_TX_AFPYEMPT_ERR_INT_CLR        | The clear bit for SPI_MST_TX_AFPYEMPT_ERR_INT interrupt. (WT)               |
| 27  | SPI_MST_RX_AFPULL_ERR_INT_CLR          | The clear bit for SPI_MST_RX_AFPULL_ERR_INT interrupt. (WT)                 |
| 26  | SPI_SIV_CMD_ERR_INT_CLR                | The clear bit for SPI_SIV_CMD_ERR_INT interrupt. (WT)                       |
| 25  | (reserved)                             |                                                                             |
| 24  | SPI_SEG_MAGIC_ERR_INT_CLR              | The clear bit for SPI_SEG_MAGIC_ERR_INT interrupt. (WT)                     |
| 23  | SPI_DMA_SEG_TRANS_DONE_INT_CLR         | The clear bit for SPI_DMA_SEG_TRANS_DONE_INT interrupt. (WT)                |
| 22  | SPI_SLV_WR_BUF_DONE_INT_CLR            | The clear bit for SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)                   |
| 21  | SPI_SLV_RD_BUF_DONE_INT_CLR            | The clear bit for SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)                   |
| 20  | SPI_TRANS_DONE_INT_CLR                 | The clear bit for SPI_TRANS_DONE_INT interrupt. (WT)                        |
| 19  | SPI_SLV_WR_DMA_DONE_INT_CLR            | The clear bit for SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)                   |
| 18  | SPI_SLV_RD_DMA_DONE_INT_CLR            | The clear bit for SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)                   |
| 17  | SPI_SLV_CMD9_INT_CLR                   | The clear bit for SPI_SLV_CMD9_INT interrupt. (WT)                          |
| 16  | SPI_SLV_CMD8_INT_CLR                   | The clear bit for SPI_SLV_CMD8_INT interrupt. (WT)                          |
| 15  | SPI_SLV_CMD7_INT_CLR                   | The clear bit for SPI_SLV_CMD7_INT interrupt. (WT)                          |
| 14  | SPI_SLV_EN_QPI_INT_CLR                 | The clear bit for SPI_SLV_EN_QPI_INT interrupt. (WT)                        |
| 13  | SPI_SLV_EX_QPI_INT_CLR                 | The clear bit for SPI_SLV_EX_QPI_INT interrupt. (WT)                        |
| 12  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR      | The clear bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)             |
| 11  | SPI_DMA_INFIFO_FULL_ERR_INT_CLR        | The clear bit for SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)               |
| 10-8| (reserved)                             |                                                                             |
| 7   | SPI_SLV_CMD_INT_CLR                    | The clear bit for SPI_SLV_CMD_INT interrupt. (WT)                           |
| 6   | SPI_SLV_CMD_INT_CLR                    | The clear bit for SPI_SLV_CMD_INT interrupt. (WT)                           |
| 5   | SPI_SLV_CMD_INT_CLR                    | The clear bit for SPI_SLV_CMD_INT interrupt. (WT)                           |
| 4   | SPI_SLV_CMD_INT_CLR                    | The clear bit for SPI_SLV_CMD_INT interrupt. (WT)                           |
| 3   | SPI_SLV_CMD_INT_CLR                    | The clear bit for SPI_SLV_CMD_INT interrupt. (WT)                           |
| 2   | SPI_SLV_CMD_INT_CLR                    | The clear bit for SPI_SLV_CMD_INT interrupt. (WT)                           |
| 1   | SPI_SLV_CMD_INT_CLR                    | The clear bit for SPI_SLV_CMD_INT interrupt. (WT)                           |
| 0   | Reset                                  |                                                                             |

SPI_DMA_INFIFO_FULL_ERR_INT_CLR The clear bit for SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR The clear bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)

SPI_SLV_EX_QPI_INT_CLR The clear bit for SPI_SLV_EX_QPI_INT interrupt. (WT)

SPI_SLV_EN_QPI_INT_CLR The clear bit for SPI_SLV_EN_QPI_INT interrupt. (WT)

SPI_SLV_CMD7_INT_CLR The clear bit for SPI_SLV_CMD7_INT interrupt. (WT)

SPI_SLV_CMD8_INT_CLR The clear bit for SPI_SLV_CMD8_INT interrupt. (WT)

SPI_SLV_CMD9_INT_CLR The clear bit for SPI_SLV_CMD9_INT interrupt. (WT)

SPI_SLV_CMD_INT_CLR The clear bit for SPI_SLV_CMD_INT interrupt. (WT)

SPI_SLV_WR_DMA_DONE_INT_CLR The clear bit for SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)

SPI_SLV_RD_DMA_DONE_INT_CLR The clear bit for SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)

SPI_SLV_WR_BUF_DONE_INT_CLR The clear bit for SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)

SPI_SLV_RD_BUF_DONE_INT_CLR The clear bit for SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)

SPI_TRANS_DONE_INT_CLR The clear bit for SPI_TRANS_DONE_INT interrupt. (WT)

SPI_DMA_SEG_TRANS_DONE_INT_CLR The clear bit for SPI_DMA_SEG_TRANS_DONE_INT interrupt. (WT)

SPI_SEG_MAGIC_ERR_INT_CLR The clear bit for SPI_SEG_MAGIC_ERR_INT interrupt. (WT)

Continued on the next page...
```