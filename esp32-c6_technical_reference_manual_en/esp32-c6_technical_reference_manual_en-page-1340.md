

```markdown
## 38.7 Application Examples

This section introduces some PARLIO application examples and their detailed operation process. All peripherals used in the examples are from ESP series chips and can work with PARLIO to form a complete data path.

**Note:**
The data paths constructed in the examples may not be the optimal. For example, users can use the SPI peripherals on two identical ESP chips to complete the peer-to-peer transfer in real case instead of using PARLIO to work with SPI. However, these examples demonstrate the flexibility of the PARLIO interface to a certain extent.

### 38.7.1 Co-working with SPI

In this example, external SPI sends data as a master device and PARLIO RX unit receives data as a slave device, and at the same time, PARLIO TX sends data as a master device and SPI receives data as a slave device, thus achieving a peer-to-peer serial data transfer.

*   Follow the operation process below to achieve SPI transmit and PARLIO receive:

    - Configure SPI clock.
    - Configure SPI as the master device.
    - Configure signal pins. Connect FSPICLK to PAD_CLK_RX, FSPICSO to RXD[16], and FSPID to RXD[0].
    - Write the data sent into the SPI buffer and configure the bit length of the data sent.
    - Set `SPI_UPDATE` to update the configured register value.
    - Reset PARLIO RX unit.
    - Configure PARLIO RX unit clock.
    - Turn off the PARLIO RX Core clock domain.
    - Configure PARLIO receive mode as sub-mode 1 of Level Enable mode. Configure RX unit data bus width as 1 bit. Configure `PARL_IO_RX_DATA_BYTELEN` according to the sending length of SPI. Set `PARL_IO_RX_REG_UPDATE`.
    - Configure PARLIO GDMA inlink list.
    - Set `PARL_IO_RX_START`.
    - Turn on the PARLIO RX Core clock domain.
    - Set `SPI_USR` to start transmitting data of SPI.
    - Poll GDMA SUC EOF interrupt.
    - Clear `PARL_IO_RX_START`.

*   Follow the operation process below to achieve PARLIO transmit and SPI receive:

    - Configure SPI clock.
    - Configure SPI as the slave device.
```