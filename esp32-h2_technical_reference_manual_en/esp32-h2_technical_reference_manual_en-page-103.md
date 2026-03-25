

# Chapter 3

## GDMA Controller (GDMA)

### 3.1 Overview

General Direct Memory Access (GDMA) is a feature that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer at high speed. The CPU is not involved in the GDMA transfer and therefore is more efficient with less workload.

The GDMA controller in ESP32-H2 has six independent channels, i.e., three transmit channels and three receive channels. These six channels are shared by peripherals with the GDMA feature, and can be assigned to any of such peripherals, including SPI2, UHCI (UART0/UART1), I2S, AES, SHA, ADC, and PARLIO. UART0 and UART1 use UHCI together.

The GDMA controller uses fixed-priority and round-robin channel arbitration schemes to manage peripherals’ needs for bandwidth.

Figure 3.1-1. Modules with GDMA Feature and GDMA Channels

| GDMA Channels | Modules |
|---------------|---------|
| Rx channel 0  | SPI2    |
| Tx channel 0  | UHCI0 (UART0/UART1) |
| Rx channel 1  | I2S     |
| Tx channel 1  | AES     |
| Rx channel 2  | SHA     |
| Tx channel 2  | ADC     |
|               | PARLIO  |

### 3.2 Features

The GDMA controller has the following features:

- AHB bus architecture
- Programmable length of data to be transferred in bytes
- Linked list of descriptors
- INCR burst transfer when accessing internal RAM
- Access to an address space of 324 KB at most in internal RAM (320 KB HP SRAM, 4 KB LP SRAM)