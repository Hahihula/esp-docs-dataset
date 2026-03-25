

```markdown
- In CPU/DMA-controlled full-/half-duplex transfer, when an external SPI master starts the SPI transfer, data on the FSPI bus is captured, converted into unit of bytes by the spi_slv_din_ctrl module, and then is stored in `spi_rx_affio`.
  - In CPU-controlled full-duplex transfer, the received data in `spi_rx_affio` will be later stored into registers `SPI_W0_REG ~ SPI_W15_REG`, successively.
  - In half-duplex Wr_BUF transfer, when the value of address (SLV_ADDR[7:0]) is received, the received data in `spi_rx_affio` will be stored in the related address of registers `SPI_W0_REG ~ SPI_W15_REG`
  - In DMA-controlled full-duplex transfer or in half-duplex Wr_DMA transfer, the received data in `spi_rx_affio` will be stored in the configured GDMA RX buffer.
- In CPU-controlled full-/half-duplex transfer, the data to send is stored in `buf_tx_affio`. In DMA-controlled full-/half-duplex transfer, the data to send is stored in `dma_tx_affio`. Therefore, Rd_BUF transaction controlled by CPU and Rd_DMA transaction controlled by DMA can be done in one slave segmented transfer. TX data comes from corresponding addresses according the transfer modes.
  - In CPU-controlled full-duplex transfer, when `SPI_SLAVE_MODE` and `SPI_DOUTDIN` are set and `SPI_DMA_TX_ENA` is cleared, the data in `SPI_W0_REG ~ SPI_W15_REG` will be stored into `buf_tx_affio`;
  - In CPU-controlled half-duplex transfer, when `SPI_SLAVE_MODE` is set, `SPI_DOUTDIN` is cleared, Rd_BUF command and SLV_ADDR[7:0] are received, the data started from the related address of `SPI_W0_REG ~ SPI_W15_REG` will be stored into `buf_tx_affio`;
  - In DMA-controlled full-duplex transfer, when `SPI_SLAVE_MODE`, `SPI_DOUTDIN` and `SPI_DMA_TX_ENA` are set, the data in the configured GDMA TX buffer will be stored into `dma_tx_affio`;
  - In DMA-controlled half-duplex transfer, when `SPI_SLAVE_MODE` is set, `SPI_DOUTDIN` is cleared, and Rd_DMA command is received, the data in the configured GDMA TX buffer will be stored into `dma_tx_affio`.

The data in `buf_tx_affio` or `dma_tx_affio` is sent out by `spi_slv_dout_ctrl` module in 1/2/4-bit modes.
```

## 29.5.9 GP-SPI2 as a Master

GP-SPI2 can be configured as a SPI master by clearing the bit `SPI_SLAVE_MODE` in `SPI_SLAVE_REG`. In this operation mode, GP-SPI2 provides clock signal (the divided clock from GP-SPI2 module clock) and six CS lines (CS0 ~ CS5).

**Note:**
- The length of transferred data must be an integral multiple of byte (8 bits), otherwise the extra bits will be lost. The extra bits here means the result of total data bits mod 8.
- To transfer bits that is not an integral multiple of byte (8 bits), consider implementing it in CMD state or ADDR state.
```