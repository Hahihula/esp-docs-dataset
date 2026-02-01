**Title: Functional Description**

- **FLASH MSPI SPI0**
- **FLASH MSPI SPI1**
- PSRAM MSPI controller
- PSRAM MSPI SPI0
- PSRAM MSPI SPI1

  - General Purpose SPI2 (GP-SPI2)
  - General Purpose SPI3 (GP-SPI3)
  - Low-Power SPI (LP-SPI)

**Feature List**

GP-SPI has the following features:

- Works as master or as slave
- Half- and full-duplex communications
- CPU- and DMA-controlled transfers
- Various data modes

  - **GP-SPI2**
    - *1-bit SPI mode*
    - *2-bit Dual SPI mode*
    - *4-bit Quad SPI mode*
    - *QPI mode*
    - *8-bit Octal SPI mode* (available only when GP-SPI2 works as a master)
    - *OPI mode* (available only when GP-SPI2 works as a master)

  - **GP-SPI3**
    - *1-bit SPI mode*
    - *2-bit Dual SPI mode*
    - *4-bit Quad SPI mode*
    - *QPI mode*

- Configurable module clock frequency
  - Master: up to 80 MHz
  - Slave: up to 60 MHz

- Configurable data length
  - CPU-controlled transfer as master or as slave: 1–64 bytes
  - DMA-controlled single transfer as master: 1–32 KB
  - DMA-controlled configurable segmented transfer as master: data length is unlimited

**Footer**
Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6