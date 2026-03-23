

# Chapter 8

## Interrupt Matrix (INTERRUPT)

### 8.1 Overview

The interrupt matrix embedded in ESP32-C3 independently routes peripheral interrupt sources to the ESP-RISC-V CPU's peripheral interrupts, to timely inform CPU to process the coming interrupts.

The ESP32-C3 has 62 peripheral interrupt sources. To map them to 31 CPU interrupts, this interrupt matrix is needed.

**Note:**
This chapter focuses on how to map peripheral interrupt sources to CPU interrupts. For more details about interrupt configuration, vector, and ISA suggested operations, please refer to Chapter 1 ESP-RISC-V CPU.

### 8.2 Features

*   Accept 62 peripheral interrupt sources as input
*   Generate 31 CPU peripheral interrupts to CPU as output
*   Query current interrupt status of peripheral interrupt sources
*   Configure priority, type, threshold, and enable signal of CPU interrupts

Figure 8.2-1 shows the structure of the interrupt matrix.

```
CPU Config
    |
Interrupt Matrix
    |          Peripheral Interrupt Sources (0 ~ 61)
    V
[CPU Interrupt Reg] <--> [Config Port / Status Port] --> [CPU Interrupt Ctrl]
    ^
    |
CPU Peripheral Interrupts (1 ~ 31)
```

Figure 8.2-1. Interrupt Matrix Structure