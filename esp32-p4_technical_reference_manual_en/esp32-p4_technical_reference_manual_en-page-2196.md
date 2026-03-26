

```markdown
Chapter 43  
SPI Controller (SPI)

43.1 Overview

The Serial Peripheral Interface (SPI) is a synchronous serial interface useful for communication with external peripherals. The ESP32-P4 chip integrates four SPI controllers:

- MSPI controller, including two sub-controllers
    - FLASH MSPI controller
        * FLASH MSPI SPI0
        * FLASH MSPI SPI1
    - PSRAM MSPI controller
        * PSRAM MSPI SPI0
        * PSRAM MSPI SPI1

- General Purpose SPI2 (GP-SPI2)
- General Purpose SPI3 (GP-SPI3)
- Low-Power SPI (LP-SPI)

MSPI controller is primarily reserved for internal use to communicate with external flash and PSRAM memory. This chapter mainly focuses on the GP-SPI and LP-SPI. In this chapter unless otherwise stated, GP-SPI refers to both GP-SPI2 and GP-SPI3.

43.2 Glossary

To better illustrate the functions of GP-SPI and LP-SPI, the following terms are used in this chapter.

| Term         | Definition                                                                 |
|--------------|-----------------------------------------------------------------------------|
| Master Mode  | GP-SPI or LP-SPI acts as an SPI master and initiates SPI transactions.     |
| Slave Mode   | GP-SPI or LP-SPI acts as an SPI slave and exchanges data with its master when its CS is asserted. |
| MISO         | Master in, slave out, data transmission from a slave to a master.           |
| MOSI         | Master out, slave in, data transmission from a master to a slave.           |
| Transaction   | One instance of a master asserting a CS line, transferring data to and from a slave, and de-asserting the CS line. Transactions are atomic, which means they can never be interrupted by another transaction. |
```