
```markdown
Register 29.21. SPI_DMA_INT_SET_REG (0x0044)

Continued from the previous page...

SPI_MST_RX_AFIFO_WFULL_ERR_INT_SET   Write 1 to set SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt. (WT)

SPI_MST_TX_AFIFO_REMPTY_ERR_INT_SET   Write 1 to set SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt. (WT)

SPI_APP2_INT_SET                       Write 1 to set SPI_APP2_INT interrupt. (WT)

SPI_APP1_INT_SET                       Write 1 to set SPI_APP1_INT interrupt. (WT)


Register 29.22. SPI_Wn_REG (n: 0-15) (0x0098 + 0x4*n)

| 31 | SPI_BUFn | 0 | Reset |
|----|----------|---|-------|
|    |          |   |       |

SPI_BUFn  32-bit data buffer n. (R/W/SS)


Register 29.23. SPI_DATE_REG (0x00F0)

| 31 | 28 | 27 | SPI_DATE | 0 | Reset |
|----|----|----|----------|---|-------|
|    |    |    |          |   |       |

SPI_DATE Version control register. (R/W)
```