
```markdown
Register 43.56. SPI_DMA_INT_CLR_REG (0x0038)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | SPI_APPI_INT_CLR                           |                                                                             |
| 29  | SPI_APP2_INT_CLR                           |                                                                             |
| 28  | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_CLR        | Write 1 to clear SPI_MST_TX_AFIFO_REMPTY_ERR_INT.                          |
| 27  | SPI_MST_RX_AFIFO_FULL_ERR_INT_CLR          | Write 1 to clear SPI_MST_RX_AFIFO_FULL_ERR_INT.                            |
| 26  | SPI_SLV_CMD_ERR_INT_CLR                    |                                                                             |
| 25  | SLV_BUF_ADDR_ERR_INT_CLR                   |                                                                             |
| 24  | (reserved)                                 |                                                                             |
| 23  | SPI_DMA_SEG_TRANS_DONE_INT_CLR             | Write 1 to clear SPI_DMA_SEG_TRANS_DONE_INT.                               |
| 22  | SPI_SLV_WR_DONE_INT_CLR                    | Write 1 to clear SPI_SLV_WR_DONE_INT.                                      |
| 21  | SPI_SLV_RD_DONE_INT_CLR                    | Write 1 to clear SPI_SLV_RD_DONE_INT.                                      |
| 20  | SPI_SLV_CMDA_DONE_INT_CLR                  | Write 1 to clear SPI_SLV_CMDA_DONE_INT.                                    |
| 19  | SPI_SLV_CMD8_DONE_INT_CLR                  | Write 1 to clear SPI_SLV_CMD8_DONE_INT.                                    |
| 18  | SPI_SLV_CMD7_DONE_INT_CLR                  | Write 1 to clear SPI_SLV_CMD7_DONE_INT.                                    |
| 17  | SPI_SLV_CMD9_DONE_INT_CLR                  | Write 1 to clear SPI_SLV_CMD9_DONE_INT.                                    |
| 16  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR          | Write 1 to clear SPI_DMA_OUTFIFO_EMPTY_ERR_INT.                           |
| 15  | SPI_DMA_INFIFO_FULL_ERR_INT_CLR            | Write 1 to clear SPI_DMA_INFIFO_FULL_ERR_INT.                              |
| 14  | (reserved)                                 |                                                                             |
| 13  | SPI_SLV_EX_QPI_INT_CLR                     | Write 1 to clear SPI_SLV_EX_QPI_INT.                                       |
| 12  | SPI_SLV_EN_QPI_INT_CLR                     | Write 1 to clear SPI_SLV_EN_QPI_INT.                                       |
| 11  | (reserved)                                 |                                                                             |
| 10  | SPI_SLV_CMD8_INT_CLR                       | Write 1 to clear SPI_SLV_CMD8_INT.                                         |
| 9   | SPI_SLV_CMD7_INT_CLR                       | Write 1 to clear SPI_SLV_CMD7_INT.                                         |
| 8   | SPI_SLV_CMD9_INT_CLR                       | Write 1 to clear SPI_SLV_CMD9_INT.                                         |
| 7   | SPI_SLV_CMDA_INT_CLR                       | Write 1 to clear SPI_SLV_CMDA_INT.                                         |
| 6   | (reserved)                                 |                                                                             |
| 5   | SPI_SLV_WR_DONE_INT_CLR                    | Write 1 to clear SPI_SLV_WR_DONE_INT.                                      |
| 4   | SPI_SLV_RD_DONE_INT_CLR                    | Write 1 to clear SPI_SLV_RD_DONE_INT.                                      |
| 3   | (reserved)                                 |                                                                             |
| 2   | SPI_DMA_SEG_TRANS_DONE_INT_CLR             | Write 1 to clear SPI_DMA_SEG_TRANS_DONE_INT.                               |
| 1   | SPI_SLV_WR_DONE_INT_CLR                    | Write 1 to clear SPI_SLV_WR_DONE_INT.                                      |
| 0   | Reset                                      |                                                                             |

SPI_DMA_INFIFO_FULL_ERR_INT_CLR    Write 1 to clear SPI_DMA_INFIFO_FULL_ERR_INT interrupt.
(WT)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR  Write 1 to clear SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt.
(WT)

SPI_SLV_EX_QPI_INT_CLR             Write 1 to clear SPI_SLV_EX_QPI_INT interrupt.
(WT)

SPI_SLV_EN_QPI_INT_CLR             Write 1 to clear SPI_SLV_EN_QPI_INT interrupt.
(WT)

SPI_SLV_CMD7_INT_CLR               Write 1 to clear SPI_SLV_CMD7_INT interrupt.
(WT)

SPI_SLV_CMD8_INT_CLR               Write 1 to clear SPI_SLV_CMD8_INT interrupt.
(WT)

SPI_SLV_CMD9_INT_CLR               Write 1 to clear SPI_SLV_CMD9_INT interrupt.
(WT)

SPI_SLV_CMDA_INT_CLR               Write 1 to clear SPI_SLV_CMDA_INT interrupt.
(WT)

SPI_SLV_RD_DMA_DONE_INT_CLR        Write 1 to clear SPI_SLV_RD_DMA_DONE_INT interrupt.
(WT)

SPI_SLV_WR_DMA_DONE_INT_CLR        Write 1 to clear SPI_SLV_WR_DMA_DONE_INT interrupt.
(WT)

SPI_SLV_RD_BUF_DONE_INT_CLR        Write 1 to clear SPI_SLV_RD_BUF_DONE_INT interrupt.
(WT)

SPI_SLV_WR_BUF_DONE_INT_CLR        Write 1 to clear SPI_SLV_WR_BUF_DONE_INT interrupt.
(WT)

Continued on the next page...
```