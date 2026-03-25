

```markdown
Register 33.9. SPI_DMA_CONF_REG (0x0030)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | SPI_DMA_OUTFIFO_EMPTY                 | Represents whether or not the DMA TX FIFO is ready for sending data.<br>0: Ready<br>1: Not ready (RO) |
| 30  | SPI_DMA_INFIFO_FULL                   | Represents whether or not the DMA RX FIFO is ready for receiving data.<br>0: Ready<br>1: Not ready (RO) |
| 29  | SPI_DMA_SLV_SEG_TRANS_EN             | Configures whether or not to enable DMA-controlled segmented transfer in slave half-duplex communication.<br>0: Disable<br>1: Enable (R/W) |
| 28  | SPI_SLV_RX_SEG_TRANS_CLR_EN           | In slave segmented transfer, if the size of the DMA RX buffer is smaller than the size of the received data,<br>1: the data in all the following Wr_DMA transactions will not be received<br>0: the data in this Wr_DMA transaction will not be received, but in the following transactions:<ul><li>if the size of DMA RX buffer is not 0, the data in following Wr_DMA transactions will be received.</li><li>if the size of DMA RX buffer is 0, the data in following Wr_DMA transactions will not be received.</li></ul>(R/W) |
| 27  | SPI_SLV_TX_SEG_TRANS_CLR_EN           | In slave segmented transfer, if the size of the DMA TX buffer is smaller than the size of the transmitted data,<br>1: the data in the following transactions will not be updated, i.e. the old data is transmitted repeatedly.<br>0: the data in this transaction will not be updated. But in the following transactions:<ul><li>if new data is filled in DMA TX FIFO, new data will be transmitted.</li><li>if no new data is filled in DMA TX FIFO, no new data will be transmitted.</li></ul>(R/W) |
| 26-17 | (reserved)                          |                                                                             |
| 16  | SPI_DMA_OUTFIFO_EMPTY                 |                                                                             |
| 15  | Reset                                 |                                                                             |
```