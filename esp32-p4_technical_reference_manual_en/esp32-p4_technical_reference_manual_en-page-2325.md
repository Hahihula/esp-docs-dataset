
```markdown
Register 43.59. SPI_DMA_INT_SET_REG (0x0044)

Continued from the previous page...

SPI_DMA_SEG_TRANSDONE_INT_SET   Write 1 to set SPI_DMA_SEG_TRANSDONE_INT interrupt.
(WT)

SPI_SLV_BUF_ADDR_ERR_INT_SET    Write 1 to set SPI_SLV_BUF_ADDR_ERR_INT interrupt.
(WT)

SPI_SLV_CMD_ERR_INT_SET         Write 1 to set SPI_SLV_CMD_ERR_INT interrupt.
(WT)

SPI_MST_RX_AFIFO_WFULL_ERR_INT_SET   Write 1 to set SPI_MST_RX_AFIFO_WFULL_ERR_INT
interrupt.
(WT)

SPI_MST_TX_AFIFO_REMPTY_ERR_INT_SET   Write 1 to set SPI_MST_TX_AFIFO_REMPTY_ERR_INT
interrupt.
(WT)

SPI_APP2_INT_SET                Write 1 to set SPI_APP2_INT interrupt.
(WT)

SPI_APP1_INT_SET               Write 1 to set SPI_APP1_INT interrupt.
(WT)


Register 43.60. SPI_WO_REG (0x0098)
```
```markdown
| 31                                                                 | SPI_BUFO |
|--------------------------------------------------------------------|----------|
|                                                                    |          |
|                                                                    | 0        |
|                                                                    | Reset    |

SPI_BUFO   32-bit data buffer 0.
(R/W/SS)
```
```markdown
Register 43.61. SPI_W1_REG (0x009C)

| 31                                                                 | SPI_BUF1 |
|--------------------------------------------------------------------|----------|
|                                                                    |          |
|                                                                    | 0        |
|                                                                    | Reset    |

SPI_BUF1   32-bit data buffer 1.
(R/W/SS)
```