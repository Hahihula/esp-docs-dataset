

```markdown
The CS high time in CONF state can be set from 62.5 µs to 3.2768 ms when fAPB_CLK is 80 MHz.
(SPI_CONF_
BITLEN + 5) will overflow from (0x40000 - SPI_CONF_BITLEN - 5) if SPI_CONF_BITLEN is larger than
0x3FFFA.

## 27.5.9 GP-SPI2 Works as a Slave

GP-SPI2 can be used as a slave to communicate with an SPI master. As a slave, GP-SPI2 supports 1-bit SPI,
2-bit dual SPI, 4-bit quad SPI, and QPI modes, with specific communication formats. To enable this mode, set
SPI_SLAVE_MODE in register SPI_SLAVE_REG.

The CS signal must be held low during the transmission, and its falling/rising edges indicate the start/end of a
single or segmented transmission. The length of transferred data must be in unit of bytes, otherwise the extra
bits will be lost. The extra bits here means the result of total bits % 8.

### 27.5.9.1 Communication Formats

In GP-SPI2 slave mode, SPI full-duplex and half-duplex communications are available. To select from the two
communications, configure SPI_DOUTDIN in register SPI_USER_REG.

Full-duplex communication means that input data and output data are transmitted simultaneously throughout
the entire transaction. All bits are treated as input or output data, which means no command, address or
dummy states are expected. The interrupt SPI_TRANS_DONE_INT is triggered once the transaction
ends.

In half-duplex communication, the format is CMD+ADDR+DUMMY+DATA (DIN or DOUT).

*   “DIN” means that an SPI master reads data from GP-SPI2.
*   “DOUT” means that an SPI master writes data to GP-SPI2.

The detailed properties of each state are as follows:

1.  CMD:
    *   Indicate the function of SPI slave;
    *   One byte from master to slave;
    *   Only the values in Table 27.5-11 and Table 27.5-12 are valid;
    *   Can be sent in 1-bit SPI mode or 4-bit QPI mode.

2.  ADDR:
    *   The address for Wr_BUF and Rd_BUF commands in CPU-controlled transfer, or placeholder bits in
        other transfers and can be defined by application;
    *   One byte from master to slave;
    *   Can be sent in 1-bit, 2-bit or 4-bit modes (according to the command).

3.  DUMMY:
    *   It’s value is meaningless. SPI slave prepares data in this state;
    *   Bit mode of FSPI bus is also meaningless here;
```