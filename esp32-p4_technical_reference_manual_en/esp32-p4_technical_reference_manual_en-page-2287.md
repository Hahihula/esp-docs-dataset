
```markdown
Register 43.20. SPI_DMA_INT_ST_REG (0x0040)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |   |   |   |   |   |   |   |   |   | (reserved) |
|     |    | SPI_APP1_INT_ST | SPI_APP2_INT_ST | SPI_MST_RX_AFIFO_ERR_INT_ST | SPI_SIV_CMD_ERR_INT_ST | SPI_SIV_BUF_ADDR_ERR_INT_ST | SPI_SIV_DMA_SENSE_ERR_INT_ST | SPI_SIV_WR_BUF_DONE_INT_ST | SPI_SIV_RD_BUF_DONE_INT_ST | SPI_SIV_CMD7_INT_ST | SPI_SIV_EN_QPI_INT_ST | SPI_SLV_EX_QPI_INT_ST | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ST | SPI_DMA_INFFIFO_FULL_ERR_INT_ST |
|     |    | (RO)             | (RO)            | (RO)                         | (RO)                     | (RO)                  | (RO)                   | (RO)                    | (RO)                      | (RO)                 | (RO)               | (RO)                | (RO)                 | (RO)                  |

SPI_DMA_INFIFO_FULL_ERR_INT_ST The interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (RO)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ST The interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (RO)

SPI_SLV_EX_QPI_INT_ST The interrupt status of SPI_SLV_EX_QPI_INT interrupt. (RO)

SPI_SLV_EN_QPI_INT_ST The interrupt status of SPI_SLV_EN_QPI_INT interrupt. (RO)

SPI_SLV_CMD7_INT_ST The interrupt status of SPI_SLV_CMD7_INT interrupt. (RO)

SPI_SLV_CMD8_INT_ST The interrupt status of SPI_SLV_CMD8_INT interrupt. (RO)

SPI_SLV_CMD9_INT_ST The interrupt status of SPI_SLV_CMD9_INT interrupt. (RO)

SPI_SLV_CMDA_INT_ST The interrupt status of SPI_SLV_CMDA_INT interrupt. (RO)

SPI_SLV_RD_DMA_DONE_INT_ST The interrupt status of SPI_SLV_RD_DMA_DONE_INT interrupt. (RO)

SPI_SLV_WR_DMA_DONE_INT_ST The interrupt status of SPI_SLV_WR_DMA_DONE_INT interrupt. (RO)

SPI_SLV_RD_BUF_DONE_INT_ST The interrupt status of SPI_SLV_RD_BUF_DONE_INT interrupt. (RO)

SPI_SLV_WR_BUF_DONE_INT_ST The interrupt status of SPI_SLV_WR_BUF_DONE_INT interrupt. (RO)

Continued on the next page...
```