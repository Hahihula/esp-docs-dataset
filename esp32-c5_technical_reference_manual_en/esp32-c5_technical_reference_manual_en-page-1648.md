

```markdown
6. Select the receive mode and enable functions required as described in Sections 43.3 and 43.5.
7. Configure GDMA inlink list.
8. Set `PARL_IO_RX_REG_UPDATE` to synchronize the register signals.
9. Set `PARL_IO_RX_START`.
10. Turn on the clock of RX Core clock domain.
11. Operate the external device to start sending data.
12. Poll the GDMA SUC EOF interrupt.
13. Clear the GDMA SUC EOF interrupt.
14. Turn off the clock of RX Core clock domain.
15. Clear `PARL_IO_RX_START`.

## 43.7.2 Data Transmitting Operation Process

This section introduces the programming procedure for transmitting data in the TX unit. Perform the following procedure to transmit parallel data from internal memory to the IO pins connected to external devices. For detailed description of the clock and reset operation restrictions in the TX unit, refer to Section 43.5.2.

1. Reset the TX unit. For specific reset scenarios and sequences, refer to Section 43.5.2.
2. Set `PARL_IO_TX_FIFO_REMPTY_INT_CLR`, `PARL_IO_TX_EOF_INT_CLR`, `PARL_IO_TX_FIFO_REMPITY_INT_ENA`, and `PARL_IO_TX_EOF_INT_ENA` consecutively.
3. Select the TXD IO pins. If a PAD clock is used, the clock IO PAD also needs to be configured.
4. Select the clock source and divide the clock by configuring PCR registers.
5. Turn off the clock of TX Core clock domain.
6. Select the functions required as described in Section 43.5.
7. Configure GDMA outlink list.
8. Poll the `PARL_IO_TX_READY`.
9. Set `PARL_IO_TX_START`.
10. Turn on the clock of TX Core clock domain.
11. Operate the external device to start receiving data.
12. Poll the `PARL_IO_TX_EOF_INT_ST`.
13. Set `PARL_IO_TX_EOF_INT_CLR`.
14. Turn off the clock of TX Core clock domain.
15. Clear `PARL_IO_TX_START`.
```