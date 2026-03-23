

# Chapter 10

## Interrupt Matrix (INTMTX)

### 10.1 Overview

The interrupt matrix embedded in ESP32-C6 independently routes peripheral interrupt sources to the ESP-RISC-V CPU’s peripheral interrupts to timely inform CPU to process the coming interrupts.

The ESP32-C6 has 77 peripheral interrupt sources that can be routed to any of the 28 CPU interrupts using the interrupt matrix.

**Note:**
This chapter focuses on how to map peripheral interrupt sources to CPU interrupts. For more details about interrupt configuration, vector, and interrupt handling operations recommended by the ISA, please refer to Chapter 1 High-Performance CPU.

### 10.2 Features

The interrupt matrix embedded in ESP32-C6 has the following features:

*   77 peripheral interrupt sources accepted as input
*   28 CPU peripheral interrupts generated to CPU as output
*   Current interrupt status query of peripheral interrupt sources
*   Multiple interrupt sources mapping to a single CPU interrupt (i.e., shared interrupts)

Figure 10.2-1 shows the structure of the interrupt matrix.