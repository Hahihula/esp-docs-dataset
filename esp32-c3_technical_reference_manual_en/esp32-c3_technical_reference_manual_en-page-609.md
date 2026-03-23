

```markdown
Full-duplex    The sending line and receiving line between the master and the slave are independent. Sending data and receiving data happen at the same time.
Half-duplex    Only one side, the master or the slave, sends data first, and the other side receives data. Sending data and receiving data can not happen at the same time.
4-line full-duplex  4-line here means: clock line, CS line, and two data lines. The two data lines can be used to send or receive data simultaneously.
4-line half-duplex  4-line here means: clock line, CS line, and two data lines. The two data lines can not be used simultaneously.
3-line half-duplex  3-line here means: clock line, CS line, and one data line. The data line is used to transmit or receive data.
1-bit SPI        In one clock cycle, one bit of data can be transferred.
(2-bit) Dual SPI  In one clock cycle, two bits of data can be transferred.
Dual Output Read  A data mode of Dual SPI. In one clock cycle, one bit of a command, or one bit of an address, or two bits of data can be transferred.
Dual I/O Read    Another data mode of Dual SPI. In one clock cycle, one bit of a command, or two bits of an address, or two bits of data can be transferred.
(4-bit) Quad SPI  In one clock cycle, four bits can be transferred.
Quad Output Read  A data mode of Quad SPI. In one clock cycle, one bit of a command, or one bit of an address, or four bits of data can be transferred.
Quad I/O Read    Another data mode of Quad SPI. In one clock cycle, one bit of a command, or four bits of an address, or four bits of data can be transferred.
QPI             In one clock cycle, four bits of a command, or four bits of an address, or four bits of data can be transferred.
```

## 27.3 Features

Some of the key features of GP-SPI2 are:

*   Master and slave modes
*   Half- and full-duplex communications
*   CPU- and DMA-controlled transfers
*   Various data modes:
    *   1-bit SPI mode
    *   2-bit Dual SPI mode
    *   4-bit Quad SPI mode
    *   QPI mode
*   Configurable module clock frequency:
```