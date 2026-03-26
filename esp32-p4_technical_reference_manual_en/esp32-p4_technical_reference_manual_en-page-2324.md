

```markdown
Register 43.59. SPI_DMA_INT_SET_REG (0x0044)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | SPI_APP1_INT_SET               |                                                                             |
| 29  | SPI_APP2_INT_SET               |                                                                             |
| 28  | SPI_MST_TX_AFIFO_ERR_INT_SET   | Write 1 to set SPI_MST_TX_AFIFO_ERR_INT interrupt. (WT)                     |
| 27  | SPI_SLV_CMD_PX_AFIFO_FULL_ERR_INT_SET | Write 1 to set SPI_SLV_CMD_PX_AFIFO_FULL_ERR_INT interrupt. (WT)         |
| 26  | SPI_SLV_CMD_PX_AFIFO_EMPTY_ERR_INT_SET | Write 1 to set SPI_SLV_CMD_PX_AFIFO_EMPTY_ERR_INT interrupt. (WT)       |
| 25  | SPI_SLV_CMD_PX_ERR_INT_SET     |                                                                             |
| 24  | SPI_SLV_BUF_ADDR_ERR_INT_SET   | Write 1 to set SPI_SLV_BUF_ADDR_ERR_INT interrupt. (WT)                     |
| 23  | SPI_DMA_OUTFIFO_ERR_INT_SET    | Write 1 to set SPI_DMA_OUTFIFO_ERR_INT interrupt. (WT)                      |
| 22  | SPI_SLV_WR_DONE_INT_SET        | Write 1 to set SPI_SLV_WR_DONE_INT interrupt. (WT)                          |
| 21  | SPI_SLV_RD_DONE_INT_SET        | Write 1 to set SPI_SLV_RD_DONE_INT interrupt. (WT)                          |
| 20  | SPI_SLV_CMD9_INT_SET           | Write 1 to set SPI_SLV_CMD9_INT interrupt. (WT)                             |
| 19  | SPI_SLV_CMD8_INT_SET           | Write 1 to set SPI_SLV_CMD8_INT interrupt. (WT)                             |
| 18  | SPI_SLV_CMD7_INT_SET           | Write 1 to set SPI_SLV_CMD7_INT interrupt. (WT)                             |
| 17  | SPI_SLV_EX_QPI_INT_SET         | Write 1 to set SPI_SLV_EX_QPI_INT interrupt. (WT)                           |
| 16  | SPI_SLV_EN_QPI_INT_SET         | Write 1 to set SPI_SLV_EN_QPI_INT interrupt. (WT)                           |
| 15  | SPI_DMA_INFIIFO_FULL_ERR_INT_SET | Write 1 to set SPI_DMA_INFIIFO_FULL_ERR_INT interrupt. (WT)               |
| 14  |                                |                                                                             |
| 13  |                                |                                                                             |
| 12  |                                |                                                                             |
| 11  |                                |                                                                             |
| 10  |                                |                                                                             |
| 9   |                                |                                                                             |
| 8   |                                |                                                                             |
| 7   |                                |                                                                             |
| 6   |                                |                                                                             |
| 5   |                                |                                                                             |
| 4   |                                |                                                                             |
| 3   |                                |                                                                             |
| 2   |                                |                                                                             |
| 1   |                                |                                                                             |
| 0   | Reset                          |                                                                             |

SPI_DMA_INFIIFO_FULL_ERR_INT_SET Write 1 to set SPI_DMA_INFIIFO_FULL_ERR_INT interrupt. (WT)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET Write 1 to set SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)

SPI_SLV_EX_QPI_INT_SET Write 1 to set SPI_SLV_EX_QPI_INT interrupt. (WT)

SPI_SLV_EN_QPI_INT_SET Write 1 to set SPI_SLV_EN_QPI_INT interrupt. (WT)

SPI_SLV_CMD7_INT_SET Write 1 to set SPI_SLV_CMD7_INT interrupt. (WT)

SPI_SLV_CMD8_INT_SET Write 1 to set SPI_SLV_CMD8_INT interrupt. (WT)

SPI_SLV_CMD9_INT_SET Write 1 to set SPI_SLV_CMD9_INT interrupt. (WT)

SPI_SLV_CMDA_INT_SET Write 1 to set SPI_SLV_CMDA_INT interrupt. (WT)

SPI_SLV_RD_DMA_DONE_INT_SET Write 1 to set SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)

SPI_SLV_WR_DMA_DONE_INT_SET Write 1 to set SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)

SPI_SLV_RD_BUF_DONE_INT_SET Write 1 to set SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)

SPI_SLV_WR_BUF_DONE_INT_SET Write 1 to set SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)

SPI_TRANS_DONE_INT_SET Write 1 to set SPI_TRANS_DONE_INT interrupt. (WT)

Continued on the next page...
```