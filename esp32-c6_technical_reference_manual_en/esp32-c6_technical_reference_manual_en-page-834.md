

```markdown
- SPI_CLK Generator: generates SPI_CLK by dividing clk_spi_mst. The divider is determined by `SPI_CLKCNT_N` and `SPI_CLKDIV_PRE`. See Section 28.7.
- SPI_CLK_out Mode Control: outputs the SPI_CLK signal for data transfer and for slaves.
- SPI_CLK_in Mode Control: captures the SPI_CLK signal from SPI master when GP-SPI2 works as a slave.

### 28.5.7.2 Data Flow Control as Master

Figure 28.5-3 shows the data flow of GP-SPI2 as master. Its control logic is as follows:

* RX data: data in FSPI bus is captured by Timing Module, converted in units of bytes by `spi_mst_din_ctrl` module, then buffered in `spi_rx_afifo`, and finally stored in corresponding addresses according to the transfer modes.
  - CPU-controlled transfer: the data is stored to registers `SPI_W0_REG ~ SPI_W15_REG`.
  - DMA-controlled transfer: the data is stored to GDMA RX buffer.

* TX data: the TX data is from corresponding addresses according to transfer modes and is saved to `buf_tx_afifo`.
  - CPU-controlled transfer: TX data is from `SPI_W0_REG ~ SPI_W15_REG`.
  - DMA-controlled transfer: TX data is from GDMA TX buffer.

The data in `buf_tx_afifo` is sent out to Timing Module in 1/2/4-bit modes, controlled by GP-SPI2 state machine. The Timing Module can be used for timing compensation. For more information, see Section 28.8.
```