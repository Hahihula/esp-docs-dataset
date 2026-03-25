

```markdown
Register 26.19. SPI_DMA_INT_RAW_REG (0x003C)

Continued from the previous page...

SPI_DMA_SEG_TRANS_DONE_INT_RAW    The raw interrupt status of SPI_DMA_SEG_TRANS_DONE_INT.
(R/WTC/SS)

SPI_SEG_MAGIC_ERR_INT_RAW          The raw interrupt status of SPI_SEG_MAGIC_ERR_INT.
(R/WTC/SS)

SPI_SLV_BUF_ADDR_ERR_INT_RAW       Raw status bit for the SPI_SLV_BUF_ADDR_ERR_INT interrupt.
1: The accessed data address during a CPU-controlled FD, Wr_BUF, or Rd_BUF transmission in
   SPI slave mode exceeds 63.
0: No address error.
(R/WTC/SS)

SPI_SLV_CMD_ERR_INT_RAW            The raw interrupt status of SPI_SLV_CMD_ERR_INT.
(R/WTC/SS)

SPI_MST_RX_AFIFO_WFULL_ERR_INT_RAW  The raw interrupt status of
SPI_MST_RX_AFIFO_WFULL_ERR_INT.
(R/WTC/SS)

SPI_MST_TX_AFIFO_REMPTY_ERR_INT_RAW The raw interrupt status of
SPI_MST_TX_AFIFO_REMPTY_ERR_INT.
(R/WTC/SS)

SPI_APP2_INT_RAW                   The raw interrupt status of SPI_APP2_INT.
The value is only controlled by the application.
(R/WTC/SS)

SPI_APP1_INT_RAW                   The raw interrupt status of SPI_APP1_INT.
The value is only controlled by the application.
(R/WTC/SS)
```