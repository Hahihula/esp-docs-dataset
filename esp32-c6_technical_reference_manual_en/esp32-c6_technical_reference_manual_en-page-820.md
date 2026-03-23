

```markdown
Chapter 28

SPI Controller (SPI)

28.1 Overview

The Serial Peripheral Interface (SPI) is a synchronous serial interface useful for communication with external peripherals. The ESP32-C6 chip integrates three SPI controllers:

*   SPI0,
*   SPI1,
*   and General Purpose SPI2 (GP-SPI2).

SPI0 and SPI1 controllers (MSPI) are primarily reserved for internal use to communicate with external flash and PSRAM memory. This chapter mainly focuses on the GP-SPI2 controller.

28.2 Glossary

To better illustrate the functions of GP-SPI2, the following terms are used in this chapter.

| Term                        | Definition                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| Master Mode                 | GP-SPI2 acts as an SPI master and initiates SPI transactions.              |
| Slave Mode                  | GP-SPI2 acts as an SPI slave and exchanges data with its master when its CS is asserted. |
| MISO                        | Master in, slave out, data transmission from a slave to a master.          |
| MOSI                        | Master out, slave in, data transmission from a master to a slave           |
| Transaction                 | One instance of a master asserting a CS line, transferring data to and from a slave, and de-asserting the CS line. Transactions are atomic, which means they can never be interrupted by another transaction. |
| SPI Transfer                | The whole process of an SPI master exchanging data with a slave.           |
| Single Transfer             | An SPI transfer that consists of only one transaction.                     |
| CPU-Controlled Transfer     | A data transfer that happens between CPU buffer `SPI_W0_REG ~ SPI_W15_REG` and SPI peripheral. |
| DMA-Controlled Transfer     | A data transfer that happens between DMA and SPI peripheral, controlled by the DMA engine. |
| Configurable Segmented Transfer | A data transfer controlled by DMA in SPI master mode. Such transfer consists of multiple transactions (segments), and each transaction can be configured independently. |
| Slave Segmented Transfer    | A data transfer controlled by DMA in SPI slave mode. Such transfer consists of multiple transactions (segments). |
```