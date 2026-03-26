

```markdown
Register 43.21. SPI_DMA_INT_SET_REG (0x0044)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | SPI_APPI_INT_SET                       | Write 1 to set SPI_APPI_INT interrupt.                                     |
| 29  | SPI_APP2_INT_SET                       | Write 1 to set SPI_APP2_INT interrupt.                                     |
| 28  | SPI_MST_TX_AFIFO_ERR_INT_SET           | Write 1 to set SPI_MST_TX_AFIFO_ERR_INT interrupt.                         |
| 27  | SPI_SLV_CMD_ERR_INT_SET                | Write 1 to set SPI_SLV_CMD_ERR_INT interrupt.                              |
| 26  | SPI_SLV_BUF_ERR_INT_SET                | Write 1 to set SPI_SLV_BUF_ERR_INT interrupt.                              |
| 25  | SPI_DMA_DONE_INT_SET                   | Write 1 to set SPI_DMA_DONE_INT interrupt.                                 |
| 24  | SPI_SLR_DONE_INT_SET                   | Write 1 to set SPI_SLR_DONE_INT interrupt.                                 |
| 23  | SPI_CMD9_DONE_INT_SET                  | Write 1 to set SPI_CMD9_DONE_INT interrupt.                                |
| 22  | SPI_CMD8_DONE_INT_SET                  | Write 1 to set SPI_CMD8_DONE_INT interrupt.                                |
| 21  | SPI_CMD7_DONE_INT_SET                  | Write 1 to set SPI_CMD7_DONE_INT interrupt.                                |
| 20  | SPI_SLV_EX_QPI_INT_SET                 | Write 1 to set SPI_SLV_EX_QPI_INT interrupt.                               |
| 19  | SPI_SLV_EN_QPI_INT_SET                 | Write 1 to set SPI_SLV_EN_QPI_INT interrupt.                               |
| 18  | SPI_DMA_INFIFO_FULL_ERR_INT_SET        | Write 1 to set SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)                  |
| 17  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET      | Write 1 to set SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)                |
| 16  | SPI_SLV_CMD8_INT_SET                   | Write 1 to set SPI_SLV_CMD8_INT interrupt.                                 |
| 15  | SPI_SLV_CMD9_INT_SET                   | Write 1 to set SPI_SLV_CMD9_INT interrupt.                                 |
| 14  | SPI_SLV_CMDA_INT_SET                   | Write 1 to set SPI_SLV_CMDA_INT interrupt.                                 |
| 13  | SPI_SLV_RD_DMA_DONE_INT_SET            | Write 1 to set SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)                      |
| 12  | SPI_SLV_WR_DMA_DONE_INT_SET            | Write 1 to set SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)                      |
| 11  | SPI_SLV_RD_BUF_DONE_INT_SET            | Write 1 to set SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)                      |
| 10  | SPI_SLV_WR_BUF_DONE_INT_SET            | Write 1 to set SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)                      |
| 9   | SPI_TRANS_DONE_INT_SET                 | Write 1 to set SPI_TRANS_DONE_INT interrupt.                               |

Continued on the next page...
```