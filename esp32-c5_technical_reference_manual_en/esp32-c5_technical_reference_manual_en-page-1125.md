

```markdown
## 33.5.8.2 Data Flow Control When GP-SPI2 Works as Master

Figure 33.5-3. Data Flow Control When GP-SPI2 Works as Master

Figure 33.5-3 shows the data flow when GP-SPI2 works as master. Its control logic is as follows:

* RX data: data bits on FSPI bus are captured by Timing Module, converted into bytes by `spi_mst_din_ctrl` module, then buffered in `spi_rx_afifo`, and finally stored in corresponding addresses according to the transfer types.
  - CPU-controlled transfer: the data is stored to registers `SPI_W0_REG ~ SPI_W15_REG`.
  - DMA-controlled transfer: the data is stored to GDMA RX buffer.
* TX data: the TX data is from corresponding addresses according to transfer modes and is saved to `buf_tx_afifo`.
  - CPU-controlled transfer: TX data is from `SPI_W0_REG~SPI_W15_REG`.
  - DMA-controlled transfer: TX data is from GDMA TX buffer.

The data in `buf_tx_afifo` is sent out to Timing Module in 1/2/4-bit modes, controlled by GP-SPI2 state machine. The Timing Module can be used for timing compensation. For more information, see Section 33.8.

## 33.5.8.3 Data Flow Control When GP-SPI2 Works as Slave

Figure 33.5-4. Data Flow Control When GP-SPI2 Works as Slave

Figure 33.5-4 shows the data flow when GP-SPI2 works as slave. Its control logic is as follows:
```