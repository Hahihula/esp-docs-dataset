

# Chapter 4

## Low-Power CPU

The ESP32-C5 Low-Power CPU (LP CPU) is a 32-bit processor based upon RISC-V ISA comprising integer (I), multiplication/division (M), atomic (A), and compressed (C) standard extensions. It features ultra-low power consumption and has a 2-stage, in-order, and scalar pipeline. The LP CPU core complex has an interrupt controller (INTC), a debug module (DM), and system bus (SYS BUS) interfaces for memory and peripheral access.

The LP CPU is in sleep mode by default (see Section 4.9). It can stay powered on when the chip enters Deep-sleep mode (see Chapter 13 Low-Power Management for details) and can access most peripherals and memories (see Chapter 6 System and Memory for details). It has two application scenarios:

*   Power insensitive scenario: When the High-Performance CPU (HP CPU) is active, the LP CPU can assist the HP CPU with some speed- and efficiency-insensitive controls and computations.
*   Power sensitive scenario: When the HP CPU is in the power-down state to save power, the LP CPU can be woken up to handle some external wake-up events.

Figure 4.0-1 shows the resources accessible to the HP CPU and the LP CPU.

![Figure 4.0-1. LP CPU Overview](image-placeholder)

In the figure above, the HP Power Domain and LP Power Domain can be powered on and off independently. When one domain is powered down, the CPU of the other domain cannot access the resources of that domain. In other words, only when the domain is powered on can its resources be accessed. For more information about power, please refer to the chapter 13 Low-Power Management.

### 4.1 Features

The LP CPU has the following features:

*   Operating clock frequency up to 20 MHz
*   One vector interrupt input