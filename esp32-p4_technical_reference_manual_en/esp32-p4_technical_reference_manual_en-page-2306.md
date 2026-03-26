

```markdown
Register 43.47. SPI_DMA_CONF_REG (0x0030)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | SPI_DMA_AFFIFO_RST | SPI_BUF_AFFIFO_RST | SPI_RX_AFFIFO_ENA | SPI_DMA_TX_ENA | SPI_DMA_RX_ENA | (reserved) | SPI_RX_EOF_EN | SPI_SLV_TX_SEG_TRAN_CLR_EN | SPI_SLV_RX_SEG_TRAN_CLR_EN | SPI_DMA_INFIFO_FULL | SPI_DMA_OUTFIFO_EMPTY | Reset |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 |

SPI_DMA_OUTFIFO_EMPTY Represents whether or not the DMA TX FIFO is ready for sending data.
- O: Ready
- 1: Not ready (RO)

SPI_DMA_INFIFO_FULL Represents whether or not the DMA RX FIFO is ready for receiving data.
- O: Ready
- 1: Not ready (RO)

SPI_DMA_SLV_SEG_TRAN_EN Configures whether or not to enable DMA-controlled segmented transfer in slave half-duplex communication.
- O: Disable
- 1: Enable (R/W)

SPI_SLV_RX_SEG_TRAN_CLR_EN In slave segmented transfer, if the size of the DMA RX buffer is smaller than the size of the received data,
- 1: the data in all the following Wr_DMA transactions will not be received
- O: the data in this Wr_DMA transaction will not be received, but in the following transactions,
    - if the size of DMA RX buffer is not 0, the data in following Wr_DMA transactions will be received.
    - if the size of DMA RX buffer is 0, the data in following Wr_DMA transactions will not be received. (R/W)

SPI_SLV_TX_SEG_TRAN_CLR_EN In slave segmented transfer, if the size of the DMA TX buffer is smaller than the size of the transmitted data,
- 1: the data in the following transactions will not be updated, i.e. the old data is transmitted repeatedly.
- O: the data in this transaction will not be updated. But in the following transactions,
    - if new data is filled in DMA TX FIFO, new data will be transmitted.
    - if no new data is filled in DMA TX FIFO, no new data will be transmitted. (R/W)

Continued on the next page...
```