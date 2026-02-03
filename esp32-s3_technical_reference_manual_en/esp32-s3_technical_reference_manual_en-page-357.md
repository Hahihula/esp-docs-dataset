**Chapter Title:**
Chapter 3

**Section Heading:**
GDMA Controller (GDMA)

**Subsection 1: Overview**

General Direct Memory Access (GDMA) is a feature that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer at a high speed. The CPU is not involved in the GDMA transfer, and therefore it becomes more efficient with less workload.

The GDMA controller in ESP32-S3 has ten independent channels, i.e., five transmit channels and five receive channels. These ten channels are shared by peripherals with GDMA feature, namely SPI2, SPI3, UHCI0, I2S0, I2S1, LCD/CAM, AES, SHA, ADC, and RMT. You can assign the ten channels to any of these peripherals. Every channel supports access to internal RAM or external RAM.

The GDMA controller uses fixed-priority and round-robin channel arbitration schemes to manage peripherals' needs for bandwidth.

**Table:**
| GDMA Channels | Modules |
|---------------|--------|
| Rx channel 0  | SPI2   |
| Tx channel 0  | SPI3   |
| Rx channel 1  | UHCI0  |
| Tx channel 1  | I2S0   |
| Rx channel 2  | I2S1   |
| Tx channel 2  | LCD/CAM|
| Rx channel 3  | AES    |
| Tx channel 3  | SHA    |
| Rx channel 4  | ADC    |
| Tx channel 4  | RMT    |

**Figure Caption:**
Figure 3.1-1. Modules with GDMA Feature and GDMA Channels

**Subsection 2: Features**

The GDMA controller has the following features:
- AHB bus architecture
- Espressif Systems

**Footer Information:**
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback