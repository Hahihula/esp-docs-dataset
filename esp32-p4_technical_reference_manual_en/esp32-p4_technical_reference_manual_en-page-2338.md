

```markdown
Register 43.85. LP_SPI_DMA_CONF_REG (0x0030)

LP_SPI_RX_AFIFO_RST Configures to reset spi_rx_afifo as shown in Figure 43.5-3 and Figure 43.5-4.
O: Not reset
1: Reset
spi_rx_afifo is used to receive data in SPI master and slave transfer.
(WT)

LP_SPI_BUF_AFIFO_RST Configures to reset buf_tx_afifo as shown in Figure 43.5-3 and Figure 43.5-4.
O: Not reset
1: Reset
buf_tx_afifo is used to send data out in CPU-controlled master and slave transfer.
(WT)
```