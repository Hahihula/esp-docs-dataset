

```markdown
Chapter 4 System and Memory

GoBack

Chapter 4

System and Memory

4.1 Overview

ESP32-H2 is an ultra-low power and highly-integrated system that integrates a high-performance 32-bit RISC-V single-core processor (CPU), four-stage pipeline, clock frequency up to 96 MHz. All internal memory, external memory, and peripherals are located on the CPU bus.

4.2 Features

• Address Space
    – 452 KB of internal memory address space accessed from the instruction bus or data bus
    – 832 KB of peripheral address space
    – 16 MB of external memory virtual address space accessed from the instruction bus or data bus
    – 320 KB of internal DMA address space

• Internal Memory
    – 128 KB internal ROM
    – 320 KB HP SRAM
    – 4 KB LP SRAM

• External Memory
    – Supports up to 16 MB external flash
    – 16 KB of Cache
    – 32 bytes of Cache block size

• Peripheral Space
    – 46 modules/peripherals in total

• GDMA
    – 8 GDMA-supported modules/peripherals

Figure 4.2-1 illustrates the system structure and address mapping.
```