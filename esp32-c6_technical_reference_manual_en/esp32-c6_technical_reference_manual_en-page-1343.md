

```markdown
Chapter 38 Parallel IO Controller (PARL_IO)          GoBack

10. Turn on the clock of TX Core clock domain.
11. Start data transfer.
12. Poll PARL_IO_TX_EOF_INT_ST.
13. Set PARL_IO_TX_EOF_INT_CLR.
14. Turn off the clock of TX Core clock domain.
15. Clear PARL_IO_TX_START.

## 38.8 Interrupts

- TX_FIFO_REMPTY_INT: Triggered when TX FIFO is empty. This interrupt indicates that there might be error in the data sent by TX.
- RX_FIFO_WFULL_INT: Triggered when RX FIFO is full. This interrupt indicates that there might be error in the data received by RX.
- TX_EOF_INT: Triggered when TX finishes sending a complete frame of data.
```