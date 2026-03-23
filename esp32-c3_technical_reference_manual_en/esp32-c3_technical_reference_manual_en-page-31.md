

# Chapter 1

## ESP-RISC-V CPU

### 1.1 Overview

ESP-RISC-V CPU is a 32-bit core based upon RISC-V ISA comprising base integer (I), multiplication/division (M) and compressed (C) standard extensions. The core has 4-stage, in-order, scalar pipeline optimized for area, power and performance. CPU core complex has an interrupt-controller (INTC), debug module (DM) and system bus (SYS BUS) interfaces for memory and peripheral access.

![Figure 1.1-1. CPU Block Diagram](image)

### 1.2 Features

* Operating clock frequency up to 160 MHz
* Zero wait cycle access to on-chip SRAM and Cache for program and data access over IRAM/DRAM interface
* Interrupt controller (INTC) with up to 31 vectored interrupts with programmable priority and threshold levels