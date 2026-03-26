

```markdown
Register 43.47. SPI_DMA_CONF_REG (0x0030)

Continued from the previous page...

SPI_RX_EOF_EN Configures the trigger source of GDMA_IN_SUC_EOF_CHn_INT_RAW.
O: GDMA_IN_SUC_EOF_CHn_INT_RAW is set by SPI_TRANSDONE_INT event in a single transfer, or by an SPI_DMA_SEG_TRANSDONE_INT event in a segmented transfer.
1: In a DAM-controlled transfer, if the bit number of transferred data is equal to (SPI_MS_DATA_BITLEN + 1), then GDMA_IN_SUC_EOF_CHn_INT_RAW will be set by hardware. (R/W)

SPI_DMA_RX_ENA Configures whether or not to enable DMA-controlled receive data transfer.
O: Disable
1: Enable
(R/W)

SPI_DMA_TX_ENA Configures whether or not to enable DMA-controlled send data transfer.
O: Disable
1: Enable
(R/W)

SPI_RX_AFIFO_RST Configures whether or not to reset RX AFIFO (i.e., spi_rx_affifo in Figure 43.5-3 and Figure 43.5-4), which is used to receive data in SPI master and slave transfer.
O: Not reset
1: Reset
(WT)

SPI_BUF_AFIFO_RST Configures whether or not to reset BUF TX AFIFO (i.e., buf_tx_affifo in Figure 43.5-3 and Figure 43.5-4), which is used to send data out in SPI slave CPU-controlled transfer and master transfer.
O: Not reset
1: Reset
(WT)

SPI_DMA_AFIFO_RST Configures whether or not to reset DMA TX AFIFO (i.e., dma_tx_affifo in Figure 43.5-3 and Figure 43.5-4), which is used to send data out in SPI slave DMA-controlled transfer.
O: Not reset
1: Reset
(WT)
```