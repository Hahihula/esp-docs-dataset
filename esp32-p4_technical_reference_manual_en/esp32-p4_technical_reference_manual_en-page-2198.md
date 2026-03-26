

```markdown
Octal I/O Read    Another data mode of Octal SPI. In one clock cycle, one bit of a command, or eight bits of an address, or eight bits of data can be transferred.

OPI               In one clock cycle, eight bits of a command, or eight bits of an address, or eight bits of data can be transferred.

SPI2              The prefix of the signals for GP-SPI2. SPI2 bus signals are routed to GPIO pins via HP GPIO matrix or HP IO MUX.

SPI3              The prefix of the signals for GP-SPI3. SPI3 bus signals are routed to GPIO pins via HP GPIO matrix only.

LP_SPI            The prefix of the signals for LP-SPI. LP_SPI bus signals are routed to GPIO pins via LP GPIO matrix only.
```

## 43.3 Features

GP-SPI has the following features:

* Works as master or as slave
* Half- and full-duplex communications
* CPU- and DMA-controlled transfers
* Various data modes

### GP-SPI2

* 1-bit SPI mode
* 2-bit Dual SPI mode
* 4-bit Quad SPI mode
* QPI mode
* 8-bit Octal SPI mode (available only when GP-SPI2 works as a master)
* OPI mode (available only when GP-SPI2 works as a master)

### GP-SPI3

* 1-bit SPI mode
* 2-bit Dual SPI mode
* 4-bit Quad SPI mode
* QPI mode

* Configurable module clock frequency
    * Master: up to 80 MHz
    * Slave: up to 60 MHz
* Configurable data length
    * CPU-controlled transfer as master or as slave: 1~64 bytes
    * DMA-controlled single transfer as master: 1~32 KB
```