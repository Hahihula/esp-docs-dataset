**Chapter Title:**
Chapter 3

**Section Heading:**
System and Memory

**Subsection 1 (Title):**
3.1 Introduction

**Body Text under Subsection 1:**
The ESP32 is a dual-core system with two Harvard Architecture Xtensa LX6 CPUs. All embedded memory, external memory and peripherals are located on the data bus and/or the instruction bus of these CPUs.

With some minor exceptions (see below), the address mapping of two CPUs is symmetric, meaning that they use the same addresses to access the same memory. Multiple peripherals in the system can access embedded memory via DMA.

The two CPUs are named "PRO_CPU" and "APP_CPU" (for “protocol” and “application”), however, for most purposes the two CPUs are interchangeable.

**Subsection 2 (Title):**
3.2 Features

**List under Subsection 2:**

- **Address Space**
  - Symmetric address mapping
  - 4 GB (32-bit) address space for both data bus and instruction bus
  - 1296 KB embedded memory address space
  - 19704 KB external memory address space
  - 512 KB peripheral address space

- **Embedded Memory**
  - Some embedded and external memory regions can be accessed by either data bus or instruction bus:
    - 328 KB DMA address space

- **Embedded Memory (Continued)**
  - 448 KB Internal ROM
  - 520 KB Internal SRAM
  - 8 KB RTC FAST Memory
  - 8 KB RTC SLOW Memory

- **External Memory**
  - Off-chip SPI memory can be mapped into the available address space as external memory. Parts of the embedded memory can be used as transparent cache for this external memory.
    - Supports up to 16 MB off-Chip SPI Flash.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information (at bottom right):**
ESP32 TRM (Version 5.6)