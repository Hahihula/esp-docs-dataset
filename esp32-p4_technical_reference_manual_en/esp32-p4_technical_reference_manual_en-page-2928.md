

```markdown
5. Set SPI_UPDATE to update the configured register value.
6. Reset PARLIO RX unit.
7. Configure PARLIO RX unit clock.
8. Turn off the PARLIO RX Core clock domain.
9. Configure PARLIO receive mode as sub-mode 1 of LEVEL Enable mode. Configure RX unit data bus width as 1 bit. Configure PARL_IO_RX_BITLEN according to the sending length of SPI. Set PARL_IO_RX_REG_UPDATE.
10. Configure PARLIO GDMA inlink list.
11. Set PARL_IO_RX_START.
12. Turn on the PARLIO RX Core clock domain.
13. Set SPI_USR to start transmitting data of SPI.
14. Poll GDMA SUC EOF interrupt.
15. Clear PARL_IO_RX_START.

• Follow the operation process below to achieve PARLIO transmit and SPI receive:
  1. Configure SPI clock.
  2. Configure SPI as the slave device.
  3. Configure signal pins. Connect FSPICLK to PAD_CLK_TX, FSPICSO to TXD[15], and FSPID to TXD[0].
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
```