

```markdown
Register 27.19. SPI_DMA_INT_RAW_REG (0x003C)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 30  | SPI_APP1_INT_RAW                          |
| 29  | SPI_APP2_INT_RAW                          |
| 28  | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_RAW       |
| 27  | SPI_MST_RX_AFIFO_FULL_ERR_INT_RAW         |
| 26  | SPI_SLV_CMD_ERR_INT_RAW                   |
| 25  | (reserved)                                |
| 24  | SPI_SEG_DMA_MAGIC_ERR_INT_RAW             |
| 23  | SPI_SEGS_TRANS_DONE_INT_RAW               |
| 22  | SPI_SLV_WR_BUF_DONE_INT_RAW               |
| 21  | SPI_SLV_RD_BUF_DONE_INT_RAW               |
| 20  | SPI_SLV_CMD9_INT_RAW                      |
| 19  | SPI_SLV_CMD8_INT_RAW                      |
| 18  | SPI_SLV_CMD7_INT_RAW                      |
| 17  | SPI_SLV_EN_QPI_INT_RAW                    |
| 16  | SPI_SLV_EX_QPI_INT_RAW                    |
| 15  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW         |
| 14  | SPI_DMA_INFIFO_FULL_ERR_INT_RAW           |
| 13  | (reserved)                                |
| 12  | SPI_SLV_WR_DMA_DONE_INT_RAW               |
| 11  | SPI_SLV_RD_DMA_DONE_INT_RAW               |
| 10  | SPI_TRANS_DONE_INT_RAW                    |
| 9   | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW         |
| 8   | SPI_DMA_INFIFO_FULL_ERR_INT_RAW           |
| 7   | (reserved)                                |
| 6   | SPI_SLV_WR_BUF_DONE_INT_RAW               |
| 5   | SPI_SLV_RD_BUF_DONE_INT_RAW               |
| 4   | SPI_SLV_CMD9_INT_RAW                      |
| 3   | SPI_SLV_CMD8_INT_RAW                      |
| 2   | SPI_SLV_CMD7_INT_RAW                      |
| 1   | SPI_SLV_EN_QPI_INT_RAW                    |
| 0   | Reset                                     |

SPI_DMA_INFIFO_FULL_ERR_INT_RAW The raw bit for SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (R/W/WTC/SS)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW The raw bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (R/W/WTC/SS)

SPI_SLV_EX_QPI_INT_RAW The raw bit for SPI_SLV_EX_QPI_INT interrupt. (R/W/WTC/SS)

SPI_SLV_EN_QPI_INT_RAW The raw bit for SPI_SLV_EN_QPI_INT interrupt. (R/W/WTC/SS)

SPI_SLV_CMD7_INT_RAW The raw bit for SPI_SLV_CMD7_INT interrupt. (R/W/WTC/SS)

SPI_SLV_CMD8_INT_RAW The raw bit for SPI_SLV_CMD8_INT interrupt. (R/W/WTC/SS)

SPI_SLV_CMD9_INT_RAW The raw bit for SPI_SLV_CMD9_INT interrupt. (R/W/WTC/SS)

SPI_SLV_CMDA_INT_RAW The raw bit for SPI_SLV_CMDA_INT interrupt. (R/W/WTC/SS)

SPI_SLV_RD_DMA_DONE_INT_RAW The raw bit for SPI_SLV_RD_DMA_DONE_INT interrupt. (R/W/WTC/SS)

SPI_SLV_WR_DMA_DONE_INT_RAW The raw bit for SPI_SLV_WR_DMA_DONE_INT interrupt. (R/W/WTC/SS)

SPI_SLV_RD_BUF_DONE_INT_RAW The raw bit for SPI_SLV_RD_BUF_DONE_INT interrupt. (R/W/WTC/SS)

SPI_SLV_WR_BUF_DONE_INT_RAW The raw bit for SPI_SLV_WR_BUF_DONE_INT interrupt. (R/W/WTC/SS)

SPI_TRANS_DONE_INT_RAW The raw bit for SPI_TRANS_DONE_INT interrupt. (R/W/WTC/SS)

Continued on the next page...
```