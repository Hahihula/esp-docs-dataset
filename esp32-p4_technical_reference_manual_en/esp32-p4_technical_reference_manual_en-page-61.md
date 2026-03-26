

# Chapter 1

## High-Performance CPU

### 1.1 Overview

ESP32-P4 is powered by Espressif’s second-generation 32-bit CPU core complex based upon RISC-V Instruction Set Architecture (ISA). The CPU Core complex consists of dual RISC-V CPU cores with a dedicated core-local interrupt controller (CLIC), a debug block, and a core-local interrupt (CLINT) timer. Figure 1.1 shows the block diagram of the CPU core complex.

![Figure 1.1-1. CPU Core Complex Block Diagram](image)

Each RISC-V core in CPU core complex uses a 5-stage, in-order, scalar pipeline architecture optimized for area, power, and performance. Each RISC-V core has a built-in dedicated core-local interrupt controller (CLIC) and system bus (SYS BUS) interfaces for memory and peripheral access. The CLINT timer is shared between two cores. The DEBUG block provides a connection between the JTAG interface and the dual cores. It also supports LP core debug. Each core also provides an instruction trace interface for offline debugging.

Espressif Systems
61
ESP32-P4 TRM
PRELIMINARY