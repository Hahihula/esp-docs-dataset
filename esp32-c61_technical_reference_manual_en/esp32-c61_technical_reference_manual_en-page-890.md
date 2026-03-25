

```markdown
## 26.5.8.1 GP-SPI2 Functional Blocks

Figure 26.5-2 shows the main functional blocks in GP-SPI2, including:

*   **Master FSM**: all the features supported in GP-SPI2 as master are controlled by this state machine together with register configuration.
*   **SPI Buffer**: SPI_WO_REG~SPI_W15_REG. See Figure 26.5-1. The data in CPU-controlled transfer is prepared in this buffer.
*   **Timing Module**: captures data on FSPI bus.
*   `spi_mst/slv_din_ctrl` and `spi_mst/slv_dout_ctrl`: converts the TX/RX data into bytes.
*   `spi_rx_afifo`: stores the received data.
*   `buf_tx_afifo`: stores the data to send.
*   `dma_tx_afifo`: stores the data from GDMA.
*   `clk_spi_mst`: this clock is divided from PLL_CLK and works as the module clock of GP-SPI2, to generate SPI_CLK signal for data transfer and for slaves, when GP-SPI2 works as master.
*   **SPI_CLK Generator**: generates SPI_CLK by dividing clk_spi_mst. The divider is determined by `SPI_CLKCNT_N` and `SPI_KDIV_PRE`.
    *   **SPI_CLK_out Mode Control**: outputs the SPI_CLK signal for data transfer and for slaves.
    *   **SPI_CLK_in Mode Control**: captures the SPI_CLK signal from SPI master when GP-SPI2 works as slave.

![Figure 26.5-2: GP-SPI2 Functional Blocks](image)
```