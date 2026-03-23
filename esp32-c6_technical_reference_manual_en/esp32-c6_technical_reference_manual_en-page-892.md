
```markdown
Register 28.21. SPI_DMA_INT_SET_REG (0x0044)

Continued from the previous page...

SPI_SLV_RD_DMA_DONE_INT_SET   Write 1 to set SPI_SLV_RD_DMA_DONE_INT interrupt. (WT)
SPI_SLV_WR_DMA_DONE_INT_SET    Write 1 to set SPI_SLV_WR_DMA_DONE_INT interrupt. (WT)
SPI_SLV_RD_BUF_DONE_INT_SET    Write 1 to set SPI_SLV_RD_BUF_DONE_INT interrupt. (WT)
SPI_SLV_WR_BUF_DONE_INT_SET    Write 1 to set SPI_SLV_WR_BUF_DONE_INT interrupt. (WT)
SPI_TRANS_DONE_INT_SET         Write 1 to set SPI_TRANS_DONE_INT interrupt. (WT)
SPI_DMA_SEG_TRANS_DONE_INT_SET Write 1 to set SPI_DMA_SEG_TRANS_DONE_INT interrupt.
(WT)

SPI_SEG_MAGIC_ERR_INT_SET      Write 1 to set SPI_SEG_MAGIC_ERR_INT interrupt. (WT)
SPI_SLV_CMD_ERR_INT_SET        Write 1 to set SPI_SLV_CMD_ERR_INT interrupt. (WT)
SPI_MST_RX_AFIFO_WFULL_ERR_INT_SET Write 1 to set SPI_MST_RX_AFIFO_WFULL_ERR_INT
interrupt. (WT)

SPI_MST_TX_AFIFO_REMPTY_ERR_INT_SET Write 1 to set SPI_MST_TX_AFIFO_REMPTY_ERR_INT
interrupt. (WT)

SPI_APP2_INT_SET               Write 1 to set SPI_APP2_INT interrupt. (WT)
SPI_APP1_INT_SET               Write 1 to set SPI_APP1_INT interrupt. (WT)


Register 28.22. SPI_Wn_REG (n: 0-15) (0x0098 + 0x4*n)

SPI_BUFn   32-bit data buffer n. (R/W/SS)


Register 28.23. SPI_DATE_REG (0x00FO)

SPI_DATE    Version control register. (R/W)
```