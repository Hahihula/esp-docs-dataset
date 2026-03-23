

```markdown
8. Set I2S_TX_STOP_EN.
9. Reset PARLIO RX unit.
10. Configure PARLIO RX unit clock.
11. Turn off PARLIO RX Core clock domain.
12. Configure PARLIO receive mode as sub-mode 10 of Pulse Enable mode. Configure the RX unit data bus width as 1 bit. Configure PARL_IO_RX_DATA_BYTELEN according to the length of the data sent by I2S. Set PARL_IO_RX_REG_UPDATE.
13. Configure PARLIO GDMA inlink list.
14. Set PARL_IO_RX_START.
15. Turn on PARLIO RX Core clock domain.
16. Set I2S_TX_START to start transmitting data.
17. Poll I2S_TX_DONE_INT.
18. Poll GDMA SUC EOF interrupt.
19. Clear I2S_TX_START.
20. Clear PARL_IO_RX_START.

## 38.7.3 Co-working with LCD

**Note:**
ESP32-C6 does not support LCD interface. For detailed descriptions about LCD control register fields mentioned below, please refer to the documentation of corresponding ESP series chips.

In this example, PARLIO TX unit sends data as a master device and external LCD controller receives data as a slave device. The I8080/MOTO6800 format is used. The specific operation process is as follows:

1. Configure signal pins. Connect CLK_TX_out to LCD pixel clock PCLK, TXD[7:0] to LCD data input pin, TXD[8] to LCD CS pin, TXD[9] to LCD CD pin.
2. Reset PARLIO TX unit.
3. Set PARL_IO_TX_FIFO_REMPTY_INT_CLR, PARL_IO_TX_EOF_INT_CLR, PARL_IO_TX_FIFO_REMPTY_INT_ENA, and PARL_IO_TX_EOF_INT_ENA in sequence.
4. Configure PARLIO TX unit clock.
5. Turn off the clock of TX Core clock domain.
6. Configure data bus width as 16 bit. Configure PARL_IO_TX_BYTELEN.
7. Configure GDMA outlink list. Note that the data sent in the linked list should conform to I8080/MOTO6800 format. The lower eight bits are valid parallel data. The 9th and 10th bits are respectively CS, CD. The MSB is the constant 1. The remaining bits are arbitrary values.
8. Poll PARL_IO_TX_READY.
9. Write 1 to PARL_IO_TX_START.
```