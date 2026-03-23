

```markdown
Register 27.20. SPI_DMA_INT_ST_REG (0x0040)

Continued from the previous page...

SPI_MST_RX_AFIFO_WFULL_ERR_INT_ST    The status bit for SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt. (RO)

SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ST   The status bit for SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt. (RO)

SPI_APP2_INT_ST   The status bit for SPI_APP2_INT interrupt. (RO)

SPI_APP1_INT_ST   The status bit for SPI_APP1_INT interrupt. (RO)


Register 27.21. SPI_W0_REG (0x0098)

31                                 0
+-----------------------------------------------+
|                                         |
+-----------------------------------------------+

SPI_BUF0    32-bit data buffer 0. (R/W/SS)


Register 27.22. SPI_W1_REG (0x009C)

31                                 0
+-----------------------------------------------+
|                                         |
+-----------------------------------------------+

SPI_BUF1    32-bit data buffer 1. (R/W/SS)


Register 27.23. SPI_W2_REG (0x00AO)

31                                 0
+-----------------------------------------------+
|                                         |
+-----------------------------------------------+

SPI_BUF2    32-bit data buffer 2. (R/W/SS)
```