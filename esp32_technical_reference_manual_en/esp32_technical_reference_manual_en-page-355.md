**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**GoBack Link:** GoBack

**Table of Features and Parameters for CS, CLK, WP, HD**

| Feature/Parameter | CS | CS | SPICSO | HSPICSO | VSPICSO |
|-------------------|----|----|--------|---------|---------|
| CLK               | CLK | CLK | SPICLK | HSPICLK | VSPICLK |
|                   | -   | -  | WP     | HSPIWP  | VSPIWP  |
|                   | -   | HD | SPIHD  | HSPIDH  | VSPIDH  |

**Section Title:**
20.2 SPI Features

**Subsection Subtitle: General Purpose SPI (GP-SPI)**

- Programmable data transfer length, in multiples of 1 byte
- Four-line full-duplex/half-duplex communication and three-line half-duplex communication support
- Master mode and slave mode
- Programmable CPOL and CPHA
- Programmable clock

**Subsection Subtitle: Parallel QSPI**

- Communication format support for specific slave devices such as flash
- Programmable communication format
- Six variations of flash-read operations available
- Automatic shift between flash and SRAM access
- Automatic wait states for flash access

**Subsection Subtitle: SPI DMA Support**

- Support for sending and receiving data using linked lists

**Subsection Subtitle: SPI Interrupt Hardware**

- SPI interrupts
- SPI DMA interrupts

**Section Title:**
20.3 GP-SPI

**Body Text:** 
The SPI master mode supports four-line full-duplex/half-duplex communication and three-line half-duplex communication. Figure 20.3-1 outlines the connections needed for four-line full-duplex/half-duplex communications.

**Footer:**
Espressif Systems
Page Number: 355
Document Version: ESP32 TRM (Version 5.6)
Submit Documentation Feedback