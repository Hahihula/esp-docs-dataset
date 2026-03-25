

```markdown
## 43.8 Application Examples

This section introduces some PARLIO application examples and their detailed operation process. All peripherals used in the examples are from ESP series chips and can work with PARLIO to form a complete data path.

**Note:**
The data paths constructed in the examples may not be the optimal. For example, users can use the SPI peripherals on two identical ESP chips to complete the peer-to-peer transfer in real case instead of using PARLIO to work with SPI. However, these examples demonstrate the flexibility of the PARLIO interface to a certain extent.

### 43.8.1 Co-working with SPI

In this example, external SPI sends data as a master device and PARLIO RX unit receives data as a slave device, and at the same time, PARLIO TX sends data as a master device and SPI receives data as a slave device, thus achieving a peer-to-peer serial data transfer.

*   Follow the operation process below to achieve SPI transmit and PARLIO receive:

    1.  Configure SPI clock.
    2.  Configure SPI as the master device.
    3.  Configure signal pins. Connect FSPICLK to PAD_CLK_RX, FSPICS0 to RXD[7], and FSPID to RXD[0].
    4.  Write the data sent into the SPI buffer and configure the bit length of the data sent.
    5.  Set `SPI_UPDATE` to update the configured register value.
    6.  Reset PARLIO RX unit.
    7.  Configure PARLIO RX unit clock.
    8.  Turn off the PARLIO RX Core clock domain.
    9.  Configure PARLIO receive mode as sub-mode 1 of Level Enable mode. Configure RX unit data bus width as 1 bit. Configure `PARL_IO_RX_BITLEN` according to the sending length of SPI. Set `PARL_IO_RX_REG_UPDATE`.
    10. Configure PARLIO GDMA inlink list.
    11. Set `PARL_IO_RX_START`.
    12. Turn on the PARLIO RX Core clock domain.
    13. Set `SPI_USR` to start transmitting data of SPI.
    14. Poll GDMA SUC EOF interrupt.
    15. Clear `PARL_IO_RX_START`.

*   Follow the operation process below to achieve PARLIO transmit and SPI receive:

    1.  Configure SPI clock.
    2.  Configure SPI as the slave device.
```