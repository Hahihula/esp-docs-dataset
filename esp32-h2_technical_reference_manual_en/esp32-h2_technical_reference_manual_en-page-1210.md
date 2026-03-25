

```markdown
- Configure signal pins. Connect FSPICLK to PAD_CLK_RX, FSPICS0 to RXD[7], and FSPID to RXD[0].
- Write the data sent into the SPI buffer and configure the bit length of the data sent.
- Set `SPI_UPDATE` to update the configured register value.
- Reset PARLIO RX unit.
- Configure PARLIO RX unit clock.
- Turn off the PARLIO RX Core clock domain.
- Configure PARLIO receive mode as sub-mode 1 of LEVEL Enable mode. Configure RX unit data bus width as 1 bit. Configure `PARL_IO_RX_BITLEN` according to the sending length of SPI. Set `PARL_IO_RX_REG_UPDATE`.
- Configure PARLIO GDMA inlink list.
- Set `PARL_IO_RX_START`.
- Turn on the PARLIO RX Core clock domain.
- Set `SPI_USR` to start transmitting data of SPI.
- Poll GDMA SUC EOF interrupt.
- Clear `PARL_IO_RX_START`.

• Follow the operation process below to achieve PARLIO transmit and SPI receive:

  - Configure SPI clock.
  - Configure SPI as the slave device.
  - Configure signal pins. Connect FSPICLK to PAD_CLK_TX, FSPICS0 to TXD[7], and FSPID to TXD[0].
  - Set `SPI_RD_BIT_ORDER` to invert the bit order.
  - Set `SPI_UPDATE` to update the configured register value.
  - Reset PARLIO TX unit.
  - Set `PARL_IO_TX_EOF_INT_CLR` and `PARL_IO_TX_EOF_INT_ENA`.
  - Configure PARLIO TX unit clock.
  - Turn off the clock of TX Core clock domain.
  - Configure data bus width as 1 bit. Write 1 to `PARL_IO_TX_VALID_OUTPUT_EN`. Configure `PARL_IO_TX_BITLEN`.
  - Configure GDMA outlink list.
  - Poll `PARL_IO_TX_READY`.
  - Write 1 to `PARL_IO_TX_START`.
  - Turn on the clock of TX Core clock domain.
  - Start data transfer.
  - Poll `PARL_IO_TX_EOF_INT_ST`.
  - Set `PARL_IO_TX_EOF_INT_CLR`.
```