

```markdown
Full-duplex    The sending line and receiving line between the master and the slave are independent. Sending data and receiving data happen at the same time.
Half-duplex    Only one side, the master or the slave, sends data, and the other side receives data. Sending data and receiving data can not happen simultaneously on one side.
4-line full-duplex  4-line here means: clock line, CS line, and two data lines. The two data lines can be used to send or receive data simultaneously.
4-line half-duplex  4-line here means: clock line, CS line, and two data lines. The two data lines can not be used simultaneously.
3-line half-duplex  3-line here means: clock line, CS line, and one data line. The data line is used to transmit or receive data.
1-bit SPI       In one clock cycle, one bit of can be transferred.
(2-bit) Dual SPI Dual Output Read    A data mode of Dual SPI. In one clock cycle, one bit of a command, or one bit of an address, or two bits of data can be transferred.
Dual I/O Read   Another data mode of Dual SPI. In one clock cycle, one bit of a command, or two bits of an address, or two bits of data can be transferred.
(4-bit) Quad SPI Quad Output Read    A data mode of Quad SPI. In one clock cycle, one bit of a command, or one bit of an address, or four bits of data can be transferred.
Quad I/O Read   Another data mode of Quad SPI. In one clock cycle, one bit of a command, or four bits of an address, or four bits of data can be transferred.
QPI            In one clock cycle, four bits of a command, or four bits of an address, or four bits of data can be transferred.
FSPI           Fast SPI. The prefix of the signals for GP-SPI2. FSPI bus signals are routed to GPIO pins via either GPIO matrix or IO MUX.
```

## 33.3 Features

GP-SPI2 has the following features:

*   Works as master or as slave
*   Half- and full-duplex communications
*   CPU- and DMA-controlled transfers
*   Various data modes

    -   1-bit SPI mode
    -   2-bit Dual SPI mode
    -   4-bit Quad SPI mode
```