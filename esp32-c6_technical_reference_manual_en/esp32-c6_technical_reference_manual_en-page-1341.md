

```markdown
- Configure signal pins. Connect FSPICLK to PAD_CLK_TX, FSPICS0 to TXD[16], and FSPID to TXD[0].
- Set SPI_RD_BIT_ORDER to invert the bit order.
- Set SPI_UPDATE to update the configured register value.

- Reset PARLIO TX unit.
  - Set PARL_IO_TX_EOF_INT_CLR and PARL_IO_TX_EOF_INT_ENA.
  - Configure PARLIO TX unit clock.
  - Turn off the clock of TX Core clock domain.
  - Configure data bus width as 1 bit. Write 1 to PARL_IO_TX_HW_VALID_EN. Configure PARL_IO_TX_BYTELEN.
  - Configure GDMA outlink list.
- Poll PARL_IO_TX_READY.

- Write 1 to PARL_IO_TX_START.
- Turn on the clock of TX Core clock domain.
- Start data transfer.
- Poll PARL_IO_TX_EOF_INT_ST.
- Set PARL_IO_TX_EOF_INT_CLR.
- Turn off the clock of TX Core clock domain.
- Clear PARL_IO_TX_START.

## 38.7.2 Co-working with I2S

In this example, external I2S sends data as a master device and PARLIO RX unit receives data as a slave device. PARLIO supports the transmission of the I2S TDM MSB alignment standard and the TDM PCM standard. When the I2S transfer protocol is the TDM MSB alignment standard, it is required to configure the receive mode of PARLIO as Lever Enable mode. When the I2S transfer protocol is the TDM PCM standard, it is required to configure the receive mode of PARLIO as the sub-mode 10 of Pulse Enable mode.

This section takes the TDM PCM alignment standard as an example. The specific operation process is as follows:

1. Configure I2S clock.
2. Configure signal pins. Connect I2SO_BCK_out to PAD_CLK_RX, I2SO_WS_out to RXD[16], and I2SO_Data_out to RXD[0].
3. Configure I2S as the master device.
4. Configure the I2S TX data mode and channel mode required. Set I2S_TX_UPDATE.
5. Reset I2S TX unit and TX FIFO.
6. Enable I2S_TX_DONE_INT.
7. Configure I2S GDMA outlink list.
```