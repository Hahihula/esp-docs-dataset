**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Titles and Content:**

1. **Title:** SPI Controller (SPI)
   - Subsection titled "30.1 Overview"
     - The Serial Peripheral Interface (SPI) is a synchronous serial interface useful for communication with external peripherals.
     - ESP32-S3 chip integrates four SPI controllers:
       - SPI0,
       - SPI1,
       - General Purpose SPI2 (GP-SPI2),
       - and General Purpose SPI3 (GP-SPI3).
     - Note: SPI0 and SPI1 are primarily reserved for internal use to communicate with external flash and PSRAM memory. This chapter mainly focuses on the GP-SPI controllers, i.e., GP-SPI2 and GP-SPI3.
   - Subsection titled "30.2 Glossary"
     - Terms used in this chapter:
       - **Master Mode:** GP-SPI acts as an SPI master and initiates SPI transactions.
       - **Slave Mode:** GP-SPI acts as an SPI slave and transfers data with its master when its CS is asserted.
       - **MISO:** Master-in, slave-out; data transmission from a slave to a master.
       - **MOSI:** Master out, slave in; data transmission from a master to a slave.
       - **Transaction:** One instance of a master asserting a CS line and transferring data between CPU and SPI peripheral. Transactions are atomic (non-interruptible).
       - **SPI Transfer:** The whole process for an SPI transfer consists only one or more transactions involving the exchange with multiple slaves, controlled by DMA engine in SPI master mode.
       - **Single Transfer:** An SPI transaction involves a single operation of data between CPU and SPI peripheral via DMA.
       - **CPU-Controlled Transfer:** A data transfer happens directly under control from CPU to SPI peripherals using specific registers (SPI_WO_REG ~ SPI_W15_REG).
       - **DMA-Controlled Transfer:** Data transfers are managed by the DMA engine, allowing multiple transactions with independent configuration of each transaction.

**Footer:**
- Page number and document version information:
  - "Espressif Systems"
  - "ESP32-S3 TRM (Version 1.7)"
  - "Submit Documentation Feedback"