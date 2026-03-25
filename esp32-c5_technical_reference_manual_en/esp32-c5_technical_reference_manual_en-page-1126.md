

```markdown
- In CPU/DMA-controlled full-/half-duplex transfer, when an external SPI master starts the SPI transfer, data on the FSPI bus is captured, converted into bytes by the spi_slv_din_ctrl module, and then is stored in `spi_rx_afifo`.

  - In CPU-controlled full-duplex transfer, the received data in `spi_rx_afifo` will be later stored into registers `SPI_W0_REG~SPI_W15_REG`, successively.

  - In half-duplex `Wr_BUF` transfer, when the value of address (SLV_ADDR[7:0]) is received, the received data in `spi_rx_afifo` will be stored in the related address of registers `SPI_W0_REG ~SPI_W15_REG`.

  - In DMA-controlled full-duplex transfer or in half-duplex `Wr_DMA` transfer, the received data in `spi_rx_afifo` will be stored in the configured GDMA RX buffer.

- In CPU-controlled full-/half-duplex transfer, the data to send is stored in `buf_tx_afifo`. In DMA-controlled full-/half-duplex transfer, the data to send is stored in `dma_tx_afifo`. Therefore, `Rd_BUF` transaction controlled by CPU and `Rd_DMA` transaction controlled by DMA can be done in one slave segmented transfer.

  - In CPU-controlled full-duplex transfer, when `SPI_SLAVE_MODE` and `SPI_DOUTDIN` are set and `SPI_DMA_TX_ENA` is cleared, the data in `SPI_W0_REG~SPI_W15_REG` will be stored into `buf_tx_afifo`.

  - In CPU-controlled half-duplex transfer, when `SPI_SLAVE_MODE` is set, `SPI_DOUTDIN` is cleared, `Rd_BUF` command and SLV_ADDR[7:0] are received, the data started from the related address of `SPI_W0_REG~SPI_W15_REG` will be stored into `buf_tx_afifo`.

  - In DMA-controlled full-duplex transfer, when `SPI_SLAVE_MODE`, `SPI_DOUTDIN`, and `SPI_DMA_TX_ENA` are set, the data in the configured GDMA TX buffer will be stored into `dma_tx_afifo`.

  - In DMA-controlled half-duplex transfer, when `SPI_SLAVE_MODE` is set, `SPI_DOUTDIN` is cleared, and `Rd_DMA` command is received, the data in the configured DMA TX buffer will be stored into `dma_tx_afifo`.

The data in `buf_tx_afifo` or `dma_tx_afifo` is sent out by `spi_slv_dout_ctrl` module in 1/2/4-bit modes.
```

## 33.5.9 GP-SPI2 Works as Master

GP-SPI2 can be configured as an SPI master by clearing the bit `SPI_SLAVE_MODE` in `SPI_SLAVE_REG`. In this operation mode, GP-SPI2 provides clock signal (the divided clock from GP-SPI module clock) and CS signal (CS0~CS5).

### 33.5.9.1 State Machine

When GP-SPI2 works as master, the state machine controls GP-SPI2’s various states during data transfer, including configuration (CONF), preparation (PREP), command (CMD), address (ADDR), dummy (DUMMY), data out (DOUT), and data in (DIN) states. GP-SPI2 is mainly used to access 1/2/4-bit SPI devices, such as flash and external RAM, thus the naming of GP-SPI2 states keeps consistent with the sequence naming of flash and external RAM. The meaning of each state is described as follows and Figure 33.5-5 shows the workflow of GP-SPI2 state machine.

1. **IDLE**: GP-SPI2 is not active or is operating as a slave.
```