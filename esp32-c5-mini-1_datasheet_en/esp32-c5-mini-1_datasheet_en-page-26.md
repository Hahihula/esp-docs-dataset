Title: Peripherals

Body Text:
aforementioned operations, but as a flexible programmable state machine, it is capable of more advanced things as well.

Subtitle: Feature List

- one BitScrambler, one channel for RX (peripheral-to-memory), one channel for TX (memory-to-peripheral). The two channels support only half-duplex communications, and cannot work at the same time
- support for memory-to-memory transfers
- process up to 32 bits per DMA clock period
- data path controlled by a BitScrambler program stored in the instruction memory
- input registers able to read 0, 8, 16, or 32 bits per clock cycle
- output registers:
  - able to write 0, 8, 16, or 32 bits per clock cycle
  - data sources for output register bits: 64 bits of input data, two counters, LUT RAM data, data output of last cycle, comparators
  - with some restrictions, each of the 32 output register bits can come from any bit on the data sources

- 8 x 257-bit instruction memory, for storing eight instructions, controlling control flow and the data path
- 2048 bytes of lookup table (LUT) memory, configurable as various word widths

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter BitScrambler.

Subtitle: Pin Assignment

Body Text:
The BitScrambler does not directly interact with IOs, so it has no pins assigned.
For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section IO Pins and [ESP32-C5 Technical Reference Manual](#) > Chapter GPIO Matrix and IO MUX.

Title: 5.2.1.14 SDIO Slave Controller

Body Text:
The SDIO Slave controller in ESP32-C5 provides hardware support for the Secure Digital Input/Output (SDIO) device interface. It allows an SDIO host to access ESP32-C5 via an SDIO bus protocol.

Subtitle: Feature List

- compatible with SDIO Physical Layer Specification V2.00 and SDIO Specifications V2.00
- support SPI, 1-bit SDIO, and 4-bit SDIO transfer modes
- clock range of 0 ~ 50 MHz
- configurable sample and drive clock edge
- integrated and SDIO-accessible registers for information interaction
- support SDIO interrupts

Footer:
Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C5-MINI-1 Datasheet v1.0  

Page Number: 26