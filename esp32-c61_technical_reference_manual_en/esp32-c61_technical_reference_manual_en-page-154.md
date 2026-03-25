

# Chapter 3
## GDMA Controller (GDMA)

### 3.1 Overview

General Direct Memory Access (GDMA) is a feature that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer at high speed. The CPU is not involved in the GDMA transfer and therefore is more efficient with less workload.

GDMA has four independent channels: two transmit channels and two receive channels. The GDMA channels are shared and can be assigned to ADC, SHA, I2S or general-purpose SPI (GP-SPI) to access internal or external memory.

GDMA uses configurable priority and weight arbitration schemes to manage peripherals' needs for bandwidth.

![Figure 3.1-1. Modules that Share GDMA Channels](image)

### 3.2 Features

GDMA has the following features:

*   AHB bus architecture
*   Programmable length of data to be transferred in bytes
*   Access via any address and size
*   Alignment:
    *   Descriptor address: 1-word aligned