

```markdown
2. Set `PARL_IO_TX_FIFO_REMPTY_INT_CLR`, `PARL_IO_TX_EOF_INT_CLR`,  
   `PARL_IO_TX_FIFO_REMPTY_INT_ENA`, and `PARL_IO_TX_EOF_INT_ENA` in sequence.
3. Select the TXD IO pins. If a PAD clock is used, the clock IO PAD also needs to be configured.
4. Select the clock source and divide the clock by configuring clock registers.
5. Turn off the clock of TX Core clock domain.
6. Select the functions required as described in Section 58.5.
7. Configure GDMA outlink list.
8. Poll the `PARL_IO_TX_READY`.
9. Set `PARL_IO_TX_START`.
10. Turn on the clock of TX Core clock domain.
11. Operate the external device to start receiving data.
12. Poll the `PARL_IO_TX_EOF_INT_ST`.
13. Set `PARL_IO_TX_EOF_INT_CLR`.
14. Turn off the clock of TX Core clock domain.
15. Clear `PARL_IO_TX_START`.

## 58.8 Application Examples

This section introduces some PARLIO application examples and their detailed operation process. All peripherals used in the examples are from ESP series chips and can work with PARLIO to form a complete data path.

**Note:**
The data paths constructed in the examples may not be the optimal. For example, users can use the SPI peripherals on two identical ESP chips to complete the peer-to-peer transfer in real case instead of using PARLIO to work with SPI. However, these examples demonstrate the flexibility of the PARLIO interface to a certain extent.

### 58.8.1 Co-working with SPI

In this example, external SPI sends data as a master device and PARLIO RX unit receives data as a slave device, and at the same time, PARLIO TX sends data as a master device and SPI receives data as a slave device, thus achieving a peer-to-peer serial data transfer.

* Follow the operation process below to achieve SPI transmit and PARLIO receive:
  1. Configure SPI clock.
  2. Configure SPI as the master device.
  3. Configure signal pins. Connect `FSPICLK` to `PAD_CLK_RX`, `FSPICSO` to `RXD[15]`, and `FSPID` to `RXD[0]`.
  4. Write the data sent into the SPI buffer and configure the bit length of the data sent.
```