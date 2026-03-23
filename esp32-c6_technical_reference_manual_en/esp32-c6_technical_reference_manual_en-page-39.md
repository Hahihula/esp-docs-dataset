

# Chapter 1

## High-Performance CPU

### 1.1 Overview

ESP-RISC-V CPU is a 32-bit core based upon RISC-V instruction set architecture (ISA) comprising base integer (I), multiplication/division (M), atomic (A) and compressed (C) standard extensions. The core has 4-stage, in-order, scalar pipeline optimized for area, power and performance. CPU core complex has a debug module (DM), interrupt-controller (INTC), core local interrupts (CLINT) and system bus (SYS BUS) interfaces for memory and peripheral access.

Figure 1.1-1. CPU Block Diagram

### 1.2 Features

*   RISC-V RV32IMAC ISA with four-stage pipeline that supports an operating clock frequency up to 160 MHz
*   Compatible with RISC-V ISA Manual Volume I: Unprivileged ISA Version 2.2 and RISC-V ISA Manual, Volume II: Privileged Architecture, Version 1.10
*   Zero wait cycle access to on-chip SRAM and Cache for program and data access over IRAM/DRAM interface