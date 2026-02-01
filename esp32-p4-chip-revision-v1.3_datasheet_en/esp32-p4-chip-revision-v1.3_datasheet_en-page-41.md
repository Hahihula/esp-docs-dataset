Title: Functional Description

- Multi-block transfer based on contiguous address, automatic reloading register configuration, shadow registers, and linked lists
- Independent configuration of multi-block transfer type for source transferer and destination transfer
- Channel disabling without data loss
- Channel suspension, resume, and abortion
- Configurable priorities among arbitration channels
- Flow control using VDMA or peripherals
- Programmable mapping between peripherals and channels

Subtitle: 4.1.2.3 2D-DMA Controller (2D-DMA)

Body Text:
The 2D-DMA controller is a DMA (Direct Memory Access) dedicated to two-dimensional image processing. In addition to all the features of GDMA-AXI, it includes support for macroblock reordering and color space conversion (CSC) to better meet the data transfer requirements from JPEG and PPA. Notably, the 2D-DMA facilitates memory-to-memory transfers, enabling the movement of macroblocks between different segments of memory address space while concurrently performing color space conversion.

Subtitle: Feature List

- One AXI master interface
- Data transfer with unaligned starting addresses
- Memory-to-memory, peripheral-to-memory (RX), and memory-to-peripheral (TX) data transfer
- Three memory-to-peripheral channels, and two peripheral-to-memory channels
- Support for PPA and JPEG Codec
- Macroblock reordering
- Color space conversion
- Configurable channel priority and weight

Subtitle: 4.1.3 Memory Organization

Body Text:
This subsection describes the memory arrangement to explain how data is stored, accessed, and managed for efficient operation.

Caption under image:
Figure 4-1 Address Mapping Structure illustrates the address mapping structure of ESP32-P4.

Footer Information:
Espressif Systems
Submit Documentation Feedback
ESP32-P4 Series Datasheet v0.6

Page Number: 
41