

```markdown
Chapter 38 Parallel IO Controller (PARL_IO) GoBack

procedure. For detailed description of the clock and reset operation restrictions for the TX unit, refer to Section 38.5.2.

1. Reset the TX unit. For specific reset scenarios and sequences, refer to Section 38.5.2.
2. Set `PARL_IO_TX_FIFO_REMPTY_INT_CLR`, `PARL_IO_TX_EOF_INT_CLR`, `PARL_IO_TX_FIFO_REMPYT_INT_ENA`, and `PARL_IO_TX_EOF_INT_ENA` consecutively.
3. Select the TXD IO pins. If a PAD clock is used, the clock IO PAD also needs to be configured.
4. Select the clock source and divide the clock by configuring PCR registers.
5. Turn off the clock of TX Core clock domain.
6. Select the functions required as described in Section 38.5.
7. Configure GDMA outlink list.
8. Poll the `PARL_IO_TX_READY`.
9. Set `PARL_IO_TX_START`.
10. Turn on the clock of TX Core clock domain.
11. Operate the external device to start receiving data.
12. Poll the `PARL_IO_TX_EOF_INT_ST`.
13. Set `PARL_IO_TX_EOF_INT_CLR`.
14. Turn off the clock of TX Core clock domain.
15. Clear `PARL_IO_TX_START`.

## 38.7 Application Examples

This section introduces some PARLIO application examples and their detailed operation process. All peripherals used in the examples are from ESP series chips and can work with PARLIO to form a complete data path.

**Note:**
The data paths constructed in the examples may not be the optimal. For example, users can use the SPI peripherals on two identical ESP chips to complete the peer-to-peer transfer in real case instead of using PARLIO to work with SPI. However, these examples demonstrate the flexibility of the PARLIO interface to a certain extent.

### 38.7.1 Co-working with SPI

In this example, external SPI sends data as a master device and PARLIO RX unit receives data as a slave device, and at the same time, PARLIO TX sends data as a master device and SPI receives data as a slave device, thus achieving a peer-to-peer serial data transfer.

* Follow the operation process below to achieve SPI transmit and PARLIO receive:
  - Configure SPI clock.
  - Configure SPI as the master device.
```