

```markdown
Register 33.21. SPI_DMA_INT_SET_REG (0x0044)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | SPI_APPI_INT_SET               | Write 1 to set the SPI_APPI_INT interrupt. (WT)                             |
| 29  | SPI_APP2_INT_SET               | Write 1 to set the SPI_APP2_INT interrupt. (WT)                             |
| 28  | SPI_MST_TX_AFIFO_ERR_INT_SET   | Write 1 to set the SPI_MST_TX_AFIFO_ERR_INT interrupt. (WT)                 |
| 27  | SPI_SLV_CMD_ERR_INT_SET        | Write 1 to set the SPI_SLV_CMD_ERR_INT interrupt. (WT)                      |
| 26  | SPI_SLV_BUF_ERR_INT_SET        | Write 1 to set the SPI_SLV_BUF_ERR_INT interrupt. (WT)                      |
| 25  | SPI_DMA_SEG_DONE_INT_SET       | Write 1 to set the SPI_DMA_SEG_DONE_INT interrupt. (WT)                     |
| 24  | SPI_TRANS_DONE_INT_SET         | Write 1 to set the SPI_TRANS_DONE_INT interrupt. (WT)                       |
| 23  | SPI_SLV_WR_DONE_INT_SET        | Write 1 to set the SPI_SLV_WR_DONE_INT interrupt. (WT)                      |
| 22  | SPI_SLV_RD_DONE_INT_SET        | Write 1 to set the SPI_SLV_RD_DONE_INT interrupt. (WT)                      |
| 21  | SPI_SLV_CMD9_DONE_INT_SET      | Write 1 to set the SPI_SLV_CMD9_DONE_INT interrupt. (WT)                   |
| 20  | SPI_SLV_CMD8_DONE_INT_SET      | Write 1 to set the SPI_SLV_CMD8_DONE_INT interrupt. (WT)                   |
| 19  | SPI_SLV_CMD7_DONE_INT_SET      | Write 1 to set the SPI_SLV_CMD7_DONE_INT interrupt. (WT)                   |
| 18  | SPI_SLV_EN_QPI_INT_SET         | Write 1 to set the SPI_SLV_EN_QPI_INT interrupt. (WT)                      |
| 17  | SPI_SLV_EX_QPI_INT_SET         | Write 1 to set the SPI_SLV_EX_QPI_INT interrupt. (WT)                      |
| 16  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET | Write 1 to set the SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)        |
| 15  | SPI_DMA_INFIFO_FULL_ERR_INT_SET | Write 1 to set the SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)             |
| 14  | SPI_SLV_CMD_ERR_INT_SET        | Write 1 to set the SPI_SLV_CMD_ERR_INT interrupt. (WT)                      |
| 13  | SPI_SLV_BUF_ERR_INT_SET        | Write 1 to set the SPI_SLV_BUF_ERR_INT interrupt. (WT)                      |
| 12  | SPI_DMA_SEG_DONE_INT_SET       | Write 1 to set the SPI_DMA_SEG_DONE_INT interrupt. (WT)                     |
| 11  | SPI_TRANS_DONE_INT_SET         | Write 1 to set the SPI_TRANS_DONE_INT interrupt. (WT)                       |
| 10  | SPI_SLV_WR_DONE_INT_SET        | Write 1 to set the SPI_SLV_WR_DONE_INT interrupt. (WT)                      |
| 9   | SPI_SLV_RD_DONE_INT_SET        | Write 1 to set the SPI_SLV_RD_DONE_INT interrupt. (WT)                      |
| 8   | SPI_SLV_CMD9_DONE_INT_SET      | Write 1 to set the SPI_SLV_CMD9_DONE_INT interrupt. (WT)                   |
| 7   | SPI_SLV_CMD8_DONE_INT_SET      | Write 1 to set the SPI_SLV_CMD8_DONE_INT interrupt. (WT)                   |
| 6   | SPI_SLV_CMD7_DONE_INT_SET      | Write 1 to set the SPI_SLV_CMD7_DONE_INT interrupt. (WT)                   |
| 5   | SPI_SLV_EN_QPI_INT_SET         | Write 1 to set the SPI_SLV_EN_QPI_INT interrupt. (WT)                      |
| 4   | SPI_SLV_EX_QPI_INT_SET         | Write 1 to set the SPI_SLV_EX_QPI_INT interrupt. (WT)                      |
| 3   | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET | Write 1 to set the SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)        |
| 2   | SPI_DMA_INFIFO_FULL_ERR_INT_SET | Write 1 to set the SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)             |
| 1   |                                |                                                                             |
| 0   | Reset                          | All bits reset to 0.                                                         |

SPI_DMA_INFIFO_FULL_ERR_INT_SET Write 1 to set the SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET Write 1 to set the SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)

SPI_SLV_EX_QPI_INT_SET Write 1 to set the SPI_SLV_EX_QPI_INT interrupt. (WT)

SPI_SLV_EN_QPI_INT_SET Write 1 to set the SPI_SLV_EN_QPI_INT interrupt. (WT)

SPI_SLV_CMD7_INT_SET Write 1 to set the SPI_SLV_CMD7_INT interrupt. (WT)

SPI_SLV_CMD8_INT_SET Write 1 to set the SPI_SLV_CMD8_INT interrupt. (WT)

SPI_SLV_CMD9_INT_SET Write 1 to set the SPI_SLV_CMD9_INT interrupt. (WT)

SPI_SLV_CMDA_INT_SET Write 1 to set the SPI_SLV_CMDA_INT interrupt. (WT)

SPI_SLV_RD_DMA_DONE_INT_SET Write 1 to set the SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)

SPI_SLV_WR_DMA_DONE_INT_SET Write 1 to set the SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)

SPI_SLV_RD_BUF_DONE_INT_SET Write 1 to set the SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)

SPI_SLV_WR_BUF_DONE_INT_SET Write 1 to set the SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)

SPI_TRANS_DONE_INT_SET Write 1 to set the SPI_TRANS_DONE_INT interrupt. (WT)
```