

```markdown
Chapter 4 System and Memory

GoBack

Chapter 4

System and Memory

4.1 Overview

ESP32-C61 has an ultra-low power and highly-integrated system with a high-performance 32-bit RISC-V processor (CPU), five-stage pipeline, clock frequency up to 160 MHz.

All internal memory, external memory, and peripherals are located on the CPU bus.

4.2 Features

• Address Space
    - 576 KB of internal memory address space, accessible by the instruction bus or data bus
    - 832 KB of peripheral address space
    - 32 MB of virtual address space for external memory, accessible by the instruction bus or data bus
    - 320 KB of internal DMA address space
    - 32 MB of external DMA address space

• Internal Memory
    - 256 KB of ROM
    - 320 KB of HP SRAM

• External Memory
    - Up to 32 MB of external flash
    - Up to 32 MB of external RAM

• Peripheral Space
    - 44 modules/peripherals in total

• GDMA
    - 4 GDMA-supported modules/peripherals

4.3 Functional Description
```