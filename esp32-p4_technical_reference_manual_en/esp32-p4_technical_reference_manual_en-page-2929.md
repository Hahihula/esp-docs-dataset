

```markdown
Chapter 58 Parallel IO Controller (PARLIO)

GoBack

58.8.2 Co-working with I2S

In this example, external I2S sends data as a master device and PARLIO RX unit receives data as a slave device. PARLIO supports the transmission of the I2S TDM MSB alignment standard and the TDM PCM standard. When the I2S transfer protocol is the TDM MSB alignment standard, it is required to configure the receive mode of PARLIO as Lever Enable mode. When the I2S transfer protocol is the TDM PCM standard, it is required to configure the receive mode of PARLIO as the sub-mode 4 of Pulse Enable mode and set `PARL_IO_RX_EXT_EN_INV`.

This section takes the TDM PCM alignment standard as an example. The specific operation process is as follows:

1. Configure I2S clock.
2. Configure signal pins. Connect I2SO_BCK_out to PAD_CLK_RX, I2SO_WS_out to RXD[15], and I2SO_Data_out to RXD[0].
3. Configure I2S as the master device.
4. Configure the I2S TX data mode and channel mode required. Set `I2S_TX_UPDATE`.
5. Reset I2S TX unit and TX FIFO.
6. Enable `I2S_TX_DONE_INT`.
7. Configure I2S GDMA outlink list.
8. Set `I2S_TX_STOP_EN`.
9. Reset PARLIO RX unit.
10. Configure PARLIO RX unit clock.
11. Turn off PARLIO RX Core clock domain.
12. Configure PARLIO receive mode as sub-mode 4 of Pulse Enable mode and set `PARL_IO_RX_EXT_EN_INV` to configure the RX unit data bus width as 1 bit. Configure `PARL_IO_TX_BITLEN` according to the length of the data sent by I2S. Set `PARL_IO_RX_REG_UPDATE`.
13. Configure PARLIO GDMA inlink list.
14. Set `PARL_IO_RX_START`.
15. Turn on PARLIO RX Core clock domain.
16. Set `I2S_TX_START` to start transmitting data.
17. Poll `I2S_TX_DONE_INT`.
18. Poll GDMA SUC EOF interrupt.
19. Clear `I2S_TX_START`.
20. Clear `PARL_IO_RX_START`.

58.8.3 Co-working with LCD

In this example, PARLIO TX unit sends data as a master device and external LCD controller receives data as a slave device. The I8080/MOTO6800 format is used. 8-bit parallel data is transferred between devices. The
```