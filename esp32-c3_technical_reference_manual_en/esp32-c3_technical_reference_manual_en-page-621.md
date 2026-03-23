

```markdown
- In DMA-controlled half-duplex transfer, when `SPI_SLAVE_MODE` is set, `SPI_DOUTDIN` is cleared, and `Rd_DMA` command is received, the data in the configured GDMA TX buffer will be stored into `dma_tx_affio`.

The data in `buf_tx_affio` or `dma_tx_affio` is sent out by `spi_slv_dout_ctrl` module in 1/2/4-bit modes.
```

## 27.5.8 GP-SPI2 Works as a Master

GP-SPI2 can be configured as a SPI master by clearing the bit `SPI_SLAVE_MODE` in `SPI_SLAVE_REG`. In this operation mode, GP-SPI2 provides clock signal (the divided clock from GP-SPI2 module clock) and six CS lines (CS0 ~ CS5).

**Note:**
- The length of transferred data must be in unit of bytes, otherwise the extra bits will be lost. The extra bits here means the result of total data bits % 8.
- To transfer bits not in unit of bytes, consider implementing it in CMD state or ADDR state.

### 27.5.8.1 State Machine

When GP-SPI2 works as a master, the state machine controls its various states during data transfer, including configuration (CONF), preparation (PREP), command (CMD), address (ADDR), dummy (DUMMY), data out (DOUT), and data in (DIN) states. GP-SPI2 is mainly used to access 1/2/4-bit SPI devices, such as flash and external RAM, thus the naming of GP-SPI2 states keeps consistent with the sequence naming of flash and external RAM. The meaning of each state is described as follows and Figure 27.5-5 shows the workflow of GP-SPI2 state machine.

1. **IDLE:** GP-SPI2 is not active or is in slave mode.
2. **CONF:** only used in DMA-controlled configurable segmented transfer. Set `SPI_USR` and `SPI_USR_CONF` to enable this state. If this state is not enabled, it means the current transfer is a single transfer.
3. **PREP:** prepare an SPI transaction and control SPI CS setup time. Set `SPI_USR` and `SPI_CS_SETUP` to enable this state.
4. **CMD:** send command sequence. Set `SPI_USR` and `SPI_USR_COMMAND` to enable this state.
5. **ADDR:** send address sequence. Set `SPI_USR` and `SPI_USR_ADDR` to enable this state.
6. **DUMMY (wait cycle):** send dummy sequence. Set `SPI_USR` and `SPI_USR_DUMMY` to enable this state.
7. **DATA:** transfer data.
    - **DOUT:** send data sequence. Set `SPI_USR` and `SPI_USR_MOSI` to enable this state.
    - **DIN:** receive data sequence. Set `SPI_USR` and `SPI_USR_MISO` to enable this state.
8. **DONE:** control SPI CS hold time. Set `SPI_USR` to enable this state.
```