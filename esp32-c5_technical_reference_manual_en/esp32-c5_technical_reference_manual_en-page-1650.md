

```markdown
3. Configure signal pins. Connect FSPICLK to PAD_CLK_TX, FSPICSO to TXD[7], and FSPID to TXD[0].
4. Set SPI_RD_BIT_ORDER to invert the bit order.
5. Set SPI_UPDATE to update the configured register value.
6. Reset PARLIO TX unit.
7. Set PARL_IO_TX_EOF_INT_CLR and PARL_IO_TX_EOF_INT_ENA.
8. Configure PARLIO TX unit clock.
9. Turn off the clock of TX Core clock domain.
10. Configure data bus width as 1 bit. Write 1 to PARL_IO_TX_VALID_OUTPUT_EN. Configure PARL_IO_TX_BITLEN.
11. Configure GDMA outlink list.
12. Poll PARL_IO_TX_READY.
13. Write 1 to PARL_IO_TX_START.
14. Turn on the clock of TX Core clock domain.
15. Start data transfer.
16. Poll PARL_IO_TX_EOF_INT_ST.
17. Set PARL_IO_TX_EOF_INT_CLR.
18. Turn off the clock of TX Core clock domain.
19. Clear PARL_IO_TX_START.

## 43.8.2 Co-working with I2S

In this example, external I2S sends data as a master device and PARLIO RX unit receives data as a slave device. PARLIO supports the transmission of the I2S TDM MSB alignment standard and the TDM PCM standard. When the I2S transfer protocol is the TDM MSB alignment standard, it is required to configure the receive mode of PARLIO as Level Enable mode. When the I2S transfer protocol is the TDM PCM standard, it is required to configure the receive mode of PARLIO as the sub-mode 10 of Pulse Enable mode and set PARL_IO_RX_EXT_EN_INV.

This section takes the TDM PCM alignment standard as an example. The specific operation process is as follows:

1. Configure I2S clock.
2. Configure signal pins. Connect I2SO_BCK_out to PAD_CLK_RX, I2SO_WS_out to RXD[7], and I2SO_Data_out to RXD[0].
3. Configure I2S as the master device.
4. Configure the I2S TX data mode and channel mode required. Set I2S_TX_UPDATE.
5. Reset I2S TX unit and TX FIFO.
6. Enable I2S_TX_DONE_INT.
7. Configure I2S GDMA outlink list.
```