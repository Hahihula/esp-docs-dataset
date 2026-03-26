

# Chapter 7

## System and Memory

### 7.1 Overview

ESP32-P4 integrates two processors:

- a high-performance 32-bit RISC-V dual-core processor (HP CPU), five-stage pipeline, clock frequency up to 400 MHz.
- a low-power 32-bit RISC-V single-core processor (LP CPU), two-stage pipeline, clock frequency up to 40 MHz.

All internal memory, external memory, and peripherals are located on the HP CPU and LP CPU buses.

### 7.2 Features

#### Address Space

- 896 KB of HP internal memory address space, accessible by the instruction bus or data bus of HP CPU via cache
- 8 KB of HP internal memory address space, accessible by the instruction bus or data bus of HP CPU
- 48 KB of LP internal memory address space, accessible by the instruction bus or data bus of LP CPU with zero latency
- 1256 KB of peripheral address space
- 64 MB of external flash virtual address space, accessible by the instruction bus or data bus
- 64 MB of external RAM virtual address space, accessible by the instruction bus or data bus
- 768 KB of internal DMA address space
- 128 MB of external DMA address space

#### Internal Memory

- 128 KB of HP ROM
- 768 KB of HP L2MEM
- 8 KB of HP SPM (Scratchpad Memory)
- 16 KB of LP ROM
- 32 KB of LP SRAM

#### External Memory