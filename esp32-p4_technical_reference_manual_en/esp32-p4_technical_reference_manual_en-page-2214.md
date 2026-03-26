

```markdown
Chapter 43 SPI Controller (SPI)

GoBack

43.5.8.3 Data Flow Control as Slave

Figure 43.5-4. Data Flow Control in GP-SPI as Slave

Figure 43.5-4 shows the data flow of GP-SPI as slave. Its control logic is as follows:

* In CPU/DMA-controlled full-/half-duplex transfer, when an external SPI master starts the SPI transfer, data on the SPI2/SPI3 bus is captured, converted into bytes by the `spi_slv_din_ctrl` module, and then is stored in `spi_rx_affo`.

  - In CPU-controlled full-duplex transfer, the received data in `spi_rx_affo` will be later stored into registers `SPI_WO_REG~SPI_W15_REG`, successively.

  - In half-duplex Wr_BUF transfer, when the value of address (SLV_ADDR[7:0]) is received, the received data in `spi_rx_affo` will be stored in the related address of registers `SPI_WO_REG ~SPI_W15_REG`.

  - In DMA-controlled full-duplex transfer or in half-duplex Wr_DMA transfer, the received data in `spi_rx_affo` will be stored in the configured DMA RX buffer.

* In CPU-controlled full-/half-duplex transfer, the data to send is stored in `buf_tx_affo`. In DMA-controlled full-/half-duplex transfer, the data to send is stored in `dma_tx_affo`. Therefore, Rd_BUF transaction controlled by CPU and Rd_DMA transaction controlled by DMA can be done in one slave segmented transfer.

  - In CPU-controlled full-duplex transfer, when `SPI_SLAVE_MODE` and `SPI_DOUTDIN` are set and `SPI_DMA_TX_ENA` is cleared, the data in `SPI_WO_REG~SPI_W15_REG` will be stored into `buf_tx_affo`.

  - In CPU-controlled half-duplex transfer, when `SPI_SLAVE_MODE` is set, `SPI_DOUTDIN` is cleared, Rd_BUF command and SLV_ADDR[7:0] are received, the data started from the related address of `SPI_WO_REG~SPI_W15_REG` will be stored into `buf_tx_affo`.

  - In DMA-controlled full-duplex transfer, when `SPI_SLAVE_MODE`, `SPI_DOUTDIN`, and `SPI_DMA_TX_ENA` are set, the data in the configured DMA TX buffer will be stored into `dma_tx_affo`.

  - In DMA-controlled half-duplex transfer, when `SPI_SLAVE_MODE` is set, `SPI_DOUTDIN` is cleared, and Rd_DMA command is received, the data in the configured DMA TX buffer will be stored into `dma_tx_affo`.
```