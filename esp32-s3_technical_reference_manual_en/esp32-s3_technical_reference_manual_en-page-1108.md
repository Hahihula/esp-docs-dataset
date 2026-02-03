**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Heading:**
30.3 Features

**Body Text:**

Some of the key features of GP-SPI are:

- Master and slave modes
- Half- and full-duplex communications
- CPU- and DMA-controlled transfers
- Various data modes:
  - **GP-SPI2:**
    * 1-bit SPI mode
    * 2-bit Dual SPI mode
    * 4-bit Quad SPI mode
    * QPI mode
    * 8-bit Octal SPI mode
    * OPI mode

  - **GP-SPI3:**
    * 1-bit SPI mode
    * 2-bit Dual SPI mode
    * 4-bit Quad SPI mode
    * QPI mode

**Subsection Heading:**
Configurable module clock frequency:

- Master: up to 80 MHz
- Slave: up to 60 MHz

**Subsection Heading:**
Configurable data length:
- CPU-controlled transfer in master mode or in slave mode: 1 ~ 64 B
- DMA-controlled single transfer in master mode: 1 ~ 32 KB
- DMA-controlled configurable segmented transfer in master mode: data length is unlimited
- DMA-controlled single transfer or segmented transfer in slave mode: data length is unlimited

**Subsection Heading:**
Configurable bit read/write order:
- Independent interrupts for CPU-controlled transfer and DMA-controlled transfer

**Subsection Heading:**
Configurable clock polarity and phase:

**Subsection Heading:**
Four SPI clock modes: mode 0 ~ mode 3

**Subsection Heading:**
Multiple CS lines in master mode:
- **GP-SPI2:** CSO ~ CS5
- **GP-SPI3:** CSO ~ CS2

**Footer Information:**
Espressif Systems  
1108 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)