

```markdown
Register 26.9. SPI_DMA_CONF_REG (0x0030)

Continued from the previous page...

SPI_RX_EOF_EN Configures the trigger source of GDMA_IN_SUC_EOF_CHn_INT_RAW.
O: GDMA_IN_SUC_EOF_CHn_INT_RAW is set by SPI_TRANS_DONE_INT event in a single transfer, or by an SPI_DMA_SEG_TRANS_DONE_INT event in a segmented transfer.
1: In a DAM-controlled transfer, if the bit number of transferred data is equal to (SPI_MS_DATA_BITLEN + 1), then GDMA_IN_SUC_EOF_CHn_INT_RAW will be set by hardware. (R/W)

SPI_DMA_RX_ENA Configures whether or not to enable DMA-controlled receive data transfer.
O: Disable
1: Enable
(R/W)

SPI_DMA_TX_ENA Configures whether or not to enable DMA-controlled send data transfer.
O: Disable
1: Enable
(R/W)

SPI_RX_AFIFO_RST Configures whether or not to reset spi_rx_afifo as shown in Figure 26.5-3 and in Figure 26.5-4.
O: Not reset
1: Reset
spi_rx_afifo is used to receive data in SPI master and slave transfer.
(WT)

SPI_BUF_AFIFO_RST Configures whether or not to reset buf_tx_afifo as shown in Figure 26.5-3 and in Figure 26.5-4.
O: Not reset
1: Reset
buf_tx_afifo is used to send data out in CPU-controlled master and slave transfer.
(WT)

SPI_DMA_AFIFO_RST Configures whether or not to reset dma_tx_afifo as shown in Figure 26.5-3 and in Figure 26.5-4.
O: Not reset
1: Reset
dma_tx_afifo is used to send data out in DMA-controlled slave transfer.
(WT)
```