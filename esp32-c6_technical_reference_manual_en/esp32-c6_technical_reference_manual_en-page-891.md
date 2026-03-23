

```markdown
Register 28.20. SPI_DMA_INT_ST_REG (0x0040)

Continued from the previous page...

SPI_MST_RX_AFIFO_WFULL_ERR_INT_ST    The interrupt status of SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt. (RO)
SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ST    The interrupt status of SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt. (RO)

SPI_APP2_INT_ST   The interrupt status of SPI_APP2_INT interrupt. (RO)
SPI_APP1_INT_ST   The interrupt status of SPI_APP1_INT interrupt. (RO)


Register 28.21. SPI_DMA_INT_SET_REG (0x0044)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| (reserved) | SPI_APP1_INT_SET | SPI_APP2_INT_SET | SPI_MST_RX_AFIFO_REMPTY_ERR_INT_SET | SPI_MST_TX_AFIFO_WFULL_ERR_INT_SET | SPI_SLV_CMD8_INT_SET | SPI_SLV_CMD9_INT_SET | SPI_SLV_CMDA_INT_SET | SPI_SLV_EX_QPI_INT_SET | SPI_SLV_EN_QPI_INT_SET | SPI_SLV_CMD7_INT_SET | SPI_SEG_DTRA_SEG_INT_DONE_SET | SPI_SLV_RX_BURF_RD_DONE_SET | SPI_SLV_RX_BURF_WR_DONE_SET | SPI_SLV_RX_BURF_WR_DONE_SET | SPI_SLV_RX_BURF_WR_DONE_SET | (reserved) | SPI_MST_RX_AFIFO_REMPTY_ERR_INT_SET | SPI_MST_TX_AFIFO_WFULL_ERR_INT_SET | SPI_APP1_INT_SET | SPI_APP2_INT_SET |
| Reset | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

SPI_DMA_INFIFO_FULL_ERR_INT_SET   Write 1 to set SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (WT)
SPI_DMA_OUTFIFO_EMPTY_ERR_INT_SET Write 1 to set SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT)
SPI_SLV_EX_QPI_INT_SET            Write 1 to set SPI_SLV_EX_QPI_INT interrupt. (WT)
SPI_SLV_EN_QPI_INT_SET            Write 1 to set SPI_SLV_EN_QPI_INT interrupt. (WT)
SPI_SLV_CMD7_INT_SET              Write 1 to set SPI_SLV_CMD7_INT interrupt. (WT)
SPI_SLV_CMD8_INT_SET              Write 1 to set SPI_SLV_CMD8_INT interrupt. (WT)
SPI_SLV_CMD9_INT_SET              Write 1 to set SPI_SLV_CMD9_INT interrupt. (WT)
SPI_SLV_CMDA_INT_SET              Write 1 to set SPI_SLV_CMDA_INT interrupt. (WT)

Continued on the next page...
```