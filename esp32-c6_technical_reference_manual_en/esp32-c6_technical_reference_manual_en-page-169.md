

# Chapter 5

## System and Memory

### 5.1 Overview

ESP32-C6 is an ultra-low power and highly-integrated system that integrates:

- a high-performance 32-bit RISC-V single-core processor (HP CPU), four-stage pipeline, clock frequency up to 160 MHz
- a low-power 32-bit RISC-V single-core processor (LP CPU), two-stage pipeline, clock frequency up to 20 MHz

All internal memory, external memory, and peripherals are located on the HP CPU and LP CPU buses.

### 5.2 Features

* **Address Space**
    - 832 KB of internal memory address space accessed from the instruction bus or data bus
    - 832 KB of peripheral address space
    - 16 MB of external memory virtual address space accessed from the instruction bus or the data bus
    - 512 KB of internal DMA address space

* **Internal Memory**
    - 320 KB internal ROM
    - 512 KB HP SRAM
    - 16 KB LP SRAM

* **External Memory**
    - Supports up to 16 MB external flash

* **Peripheral Space**
    - 51 modules/peripherals in total

* **GDMA**
    - 8 GDMA-supported modules/peripherals

Figure 5.2-1 illustrates the system structure and address mapping.