Title: Functional Description

Body Text:
independent channels, three transmit and three receive. These channels are shared by peripherals with the GDMA feature, such as SPI2, UHCI (UARTO/UART1), I2S, AES, SHA, ADC, and PARLIO.

Subtitle: Feature List

- Programmable length of data to be transferred in bytes
- Linked list of descriptors for efficient data transfer management
- INCR burst transfer when accessing internal RAM for improved performance
- Access to an address space of up to 384 KB in internal RAM
- Software-configurable selection of peripheral requesting service
- Fixed-priority and round-robin channel arbitration schemes for managing bandwidth
- Support for Event Task Matrix

For details, see [ESP32-C6 Technical Reference Manual > Chapter GDMA Controller (DMA)](#).

Subtitle: 4.1.2 Memory Organization

Body Text:
This subsection describes the memory arrangement to explain how data is stored, accessed, and managed for efficient operation.

Figure Caption:
Figure 4-1 illustrates the address mapping structure of ESP32-C6.
- [Image Description]: The image shows a block diagram labeled "Figure 4-1. Address Mapping Structure" with various components such as CPU HP, ROM (320KB), MMU, External Memory, and Peripherals connected by lines indicating memory addresses.

Footer:
Espressif Systems
ESP32-C6 Series Datasheet v1.4

Page Number: 
39

Link Text at the bottom right corner of page 38/39 (not fully visible):
Submit Documentation Feedback