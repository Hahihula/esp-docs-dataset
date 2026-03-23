

# Chapter 3

## Low-Power CPU

The ESP32-C6 Low-Power CPU (LP CPU) is a 32-bit processor based upon RISC-V ISA comprising integer (I), multiplication/division (M), atomic (A), and compressed (C) standard extensions. It features ultra-low power consumption and has a 2-stage, in-order, and scalar pipeline. The LP CPU core complex has an interrupt controller (INTC), a debug module (DM), and system bus (SYS BUS) interfaces for memory and peripheral access.

The LP CPU is in sleep mode by default (see Section 3.9). It can stay powered on when the chip enters Deep-sleep mode (see Chapter 12 Low-Power Management for details) and can access most peripherals and memories (see Chapter 5 System and Memory for details). It has two application scenarios:

*   Power insensitive scenario: When the High-Performance CPU (HP CPU) is active, the LP CPU can assist the HP CPU with some speed- and efficiency-insensitive controls and computations.
*   Power sensitive scenario: When the HP CPU is in the power-down state to save power, the LP CPU can be woken up to handle some external wake-up events.

![Figure 3.0-1. LP CPU Overview](image)

## 3.1 Features

The LP CPU has the following features:

*   Operating clock frequency up to 20 MHz
*   1 vector interrupts
*   Debug module compliant with RISC-V External Debug Support Version 0.13 with external debugger support over an industry-standard JTAG/USB port
*   Hardware trigger compliant with RISC-V External Debug Support Version 0.13 with up to 2 breakpoints/watchpoints