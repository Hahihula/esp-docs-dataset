

```markdown
- If the length of the configured DMA RX buffer is longer than that of the actual data transferred, the RX buffer is not fully used, and the remaining buffer is discarded. In the following transaction, a new linked buffer will be used directly.

## 43.5.8 Data Flow Control (Take GP-SPI as an Example)

CPU-controlled and DMA-controlled transfers are supported in GP-SPI both as master and as slave.
CPU-controlled transfer means that data is transferred between registers `SPI_W0_REG~SPI_W15_REG` and the SPI device. DMA-controlled transfer means that data is transferred between the configured DMA TX/RX buffer and the SPI device. To select between the two transfer types, configure `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA` before the transfer starts.

### 43.5.8.1 GP-SPI Functional Blocks

Figure 43.5-2 shows the main functional blocks in GP-SPI, including:

*   Master FSM: all the features supported in GP-SPI as master are controlled by this state machine together with register configuration.
*   SPI Buffer: `SPI_W0_REG~SPI_W15_REG`, See Figure 43.5-1. The data in the CPU-controlled transfer is prepared in this buffer.
*   Timing Module: captures data on SPI2/SPI3 bus.
*   `spi_mst/slv_din_ctrl` and `spi_mst/slv_dout_ctrl`: converts the TX/RX data into bytes.
*   `spi_rx_afifo`: stores the received data.
*   `buf_tx_afifo`: stores the data to send.
*   `dma_tx_afifo`: stores the data from DMA.
*   `clk_spi_mst`: this clock is the module clock of GP-SPI and is used in GP-SPI as master to generate SPI_CLK signal for data transfer and for slaves.
*   SPI_CLK Generator: generates SPI_CLK by dividing clk_spi_mst. The divider is determined by `SPI_CLKCNT_N` and `SPI_CLKDIV_PRE`.
```