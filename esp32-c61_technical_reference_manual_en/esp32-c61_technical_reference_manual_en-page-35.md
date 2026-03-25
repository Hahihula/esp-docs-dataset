

# Chapter 1

## ESP-RISC-V CPU

### 1.1 Overview

ESP32-C61 is powered by Espressif's second-generation 32-bit CPU core complex based upon RISC-V Instruction Set Architecture (ISA). The CPU Core complex consists of a RISC-V CPU core with a dedicated core-local interrupt controller (CLIC), a debug block, and a core-local interrupt (CLINT) timer. Figure 1.1 shows the block diagram of the CPU core complex.

![Figure 1.1-1. CPU Core Complex Block Diagram](image)

**Figure 1.1-1. CPU Core Complex Block Diagram**

RISC-V core in CPU core complex uses a 5-stage, in-order, scalar pipeline architecture optimized for area, power, and performance. RISC-V core also has built-in dedicated core-local interrupt controller (CLIC) and system bus (SYS BUS) interfaces for memory and peripheral access. The DEBUG block provides a connection between the JTAG interface and the RISC-V core. The core also provides an instruction trace interface for offline debugging.

### 1.2 Features

RISC-V HP CPU core in the CPU core complex implements the following standard RISC-V extensions: