

```markdown
Chapter 58 Parallel IO Controller (PARLIO)	GoBack

specific operation process is as follows:

1. Configure signal pins. Connect CLK_TX_out to LCD pixel clock PCLKX, TXD[7:0] to LCD data input pin, TXD[8] to LCD CS pin, TXD[9] to LCD CD pin.

2. Reset PARLIO TX unit.

3. Set `PARL_IO_TX_FIFO_REMPTY_INT_CLR`, `PARL_IO_TX_EOF_INT_CLR`, `PARL_IO_TX_FIFO_REMPPTY_INT_ENA`, and `PARL_IO_TX_EOF_INT_ENA` in sequence.

4. Configure PARLIO TX unit clock.

5. Turn off the clock of TX Core clock domain.

6. Configure data bus width as 16 bit. Configure `PARL_IO_TX_BITLEN`.

7. Configure GDMA outlink list. Note that the data sent in the linked list should conform to I8080/MOTO6800 format. The lower eight bits are valid parallel data. The 9th and 10th bits are respectively CS, CD. The MSB is the constant 1. The remaining bits are arbitrary values.

8. Poll `PARL_IO_TX_READY`.

9. Write 1 to `PARL_IO_TX_START`.

10. Turn on the clock of TX Core clock domain.

11. Start data transfer.

12. Poll `PARL_IO_TX_EOF_INT_ST`.

13. Set `PARL_IO_TX_EOF_INT_CLR`.

14. Turn off the clock of TX Core clock domain.

15. Clear `PARL_IO_TX_START`.
```