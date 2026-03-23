

```markdown
Register 27.9. SPI_DMA_CONF_REG (0x0030)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                       |                                                                             |
| 30  | SPI_DMA_AFIFO_RST                    | Set this bit to reset dma_tx_afifo as shown in Figure 27.5-3 and in Figure 27.5-4. dma_tx_afifo is used to send data out in DMA-controlled slave transfer. (WT) |
| 29  | SPI_BUF_AFIFO_RST                    | Set this bit to reset buf_tx_afifo as shown in Figure 27.5-3 and in Figure 27.5-4. buf_tx_afifo is used to send data out in CPU-controlled master and slave transfer. (WT) |
| 28  | SPI_RX_AFIFO_RST                     | Set this bit to reset spi_rx_afifo as shown in Figure 27.5-3 and in Figure 27.5-4. spi_rx_afifo is used to receive data in SPI master and slave transfer. (WT) |
| 27  | SPI_DMA_RX_ENA                       | Set this bit to enable SPI DMA controlled receive data mode. (R/W)            |
| 26  | SPI_DMA_TX_ENA                       | Set this bit to enable SPI DMA controlled send data mode. (R/W)               |
| 25  | SPI_SLV_RX_SEG_TRAN_CLR_EN           | In DMA-controlled half-duplex slave mode, if the size of DMA RX buffer is smaller than the size of the received data, 1: the data in following transfers will not be received. O: the data in this transfer will not be received, but in the following transfers, if the size of DMA RX buffer is not O, the data in following transfers will be received, otherwise not. (R/W) |
| 24  | SPI_SLV_TX_SEG_TRAN_CLR_EN           | In DMA-controlled half-duplex slave mode, if the size of DMA TX buffer is smaller than the size of the transmitted data, 1: the data in the following transfers will not be updated, i.e. the old data is transmitted repeatedly. O: the data in this transfer will not be updated. But in the following transfers, if new data is filled in DMA TX FIFO, new data will be transmitted, otherwise not. (R/W) |
| 23  | SPI_RX_EOF_EN                        | In a DAM-controlled transfer, if the bit number of transferred data is equal to (SPI_MS_DATA_BITLEN + 1), then GDMA_IN_SUC_EOF_CHn_INT_RAW will be set by hardware. O: GDMA_IN_SUC_EOF_CHn_INT_RAW is set by SPI_TRANSDONE_INT event in a non-segmented transfer, or by in a SPI_DMA_SEG_TRANSDONE_INT event in a segmented transfer. (R/W) |
| 22  |                                       |                                                                             |
| 21  | SPI_RX_EOF_EN                        |                                                                             |
| 20  | SPI_SLV_TX_SEG_TRAN_CLR_EN           |                                                                             |
| 19  | SPI_SLV_RX_SEG_TRAN_CLR_EN           |                                                                             |
| 18  | SPI_TX_TX_SEG_TRAN_CLR_EN            |                                                                             |
| 17  | SPI_DMA_SIV_SEG_TRAN_EN              |                                                                             |

SPI_DMA_SLV_SEG_TRAN_EN: 1: enable DAM-controlled segmented transfer in slave half-duplex mode. O: disable. (R/W)

SPI_RX_EOF_EN: In a DAM-controlled transfer, if the bit number of transferred data is equal to (SPI_MS_DATA_BITLEN + 1), then GDMA_IN_SUC_EOF_CHn_INT_RAW will be set by hardware. O: GDMA_IN_SUC_EOF_CHn_INT_RAW is set by SPI_TRANSDONE_INT event in a non-segmented transfer, or by in a SPI_DMA_SEG_TRANSDONE_INT event in a segmented transfer. (R/W)

SPI_DMA_RX_ENA: Set this bit to enable SPI DMA controlled receive data mode. (R/W)

SPI_DMA_TX_ENA: Set this bit to enable SPI DMA controlled send data mode. (R/W)

SPI_SLV_RX_SEG_TRAN_CLR_EN: In DMA-controlled half-duplex slave mode, if the size of DMA RX buffer is smaller than the size of the received data, 1: the data in following transfers will not be received. O: the data in this transfer will not be received, but in the following transfers, if the size of DMA RX buffer is not O, the data in following transfers will be received, otherwise not. (R/W)

SPI_SLV_TX_SEG_TRAN_CLR_EN: In DMA-controlled half-duplex slave mode, if the size of DMA TX buffer is smaller than the size of the transmitted data, 1: the data in the following transfers will not be updated, i.e. the old data is transmitted repeatedly. O: the data in this transfer will not be updated. But in the following transfers, if new data is filled in DMA TX FIFO, new data will be transmitted, otherwise not. (R/W)

SPI_RX_EOF_EN: In a DAM-controlled transfer, if the bit number of transferred data is equal to (SPI_MS_DATA_BITLEN + 1), then GDMA_IN_SUC_EOF_CHn_INT_RAW will be set by hardware. O: GDMA_IN_SUC_EOF_CHn_INT_RAW is set by SPI_TRANSDONE_INT event in a non-segmented transfer, or by in a SPI_DMA_SEG_TRANSDONE_INT event in a segmented transfer. (R/W)

SPI_DMA_RX_ENA: Set this bit to enable SPI DMA controlled receive data mode. (R/W)

SPI_DMA_TX_ENA: Set this bit to enable SPI DMA controlled send data mode. (R/W)
```