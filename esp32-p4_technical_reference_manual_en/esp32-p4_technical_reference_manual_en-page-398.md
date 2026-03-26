

# Chapter 6

## 2D-DMA Controller (2D-DMA)

### 6.1 Overview

The 2D-DMA controller is a DMA (Direct Memory Access) dedicated to two-dimensional image processing. In addition to all the features of GDMA-AXI, it includes support for macroblock reordering and color space conversion (CSC) to better meet the data transfer requirements from JPEG and PPA. Notably, the 2D-DMA facilitates memory-to-memory transfers, enabling the movement of macroblocks between different segments of memory address space while concurrently performing color space conversion.

### 6.2 Features

- One AXI master interface
- Data transfer with unaligned starting addresses
- Memory-to-memory, peripheral-to-memory (RX), and memory-to-peripheral (TX) data transfer
- Four memory-to-peripheral channels, and three peripheral-to-memory channels
- Support for PPA and JPEG Codec
- Macroblock reordering
- Color space conversion
- Configurable channel priority and weight

### 6.3 Architecture

In ESP32-P4, only JPEG Codec and PPA support 2D-DMA. The 2D-DMA controller and CPU data bus have access to the same address space in memory. Figure 6.3-1 shows the basic architecture of the 2D-DMA controller.