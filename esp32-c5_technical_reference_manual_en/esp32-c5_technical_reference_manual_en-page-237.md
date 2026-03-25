

```markdown
Chapter 6 System and Memory

GoBack

Chapter 6

System and Memory

6.1 Overview

ESP32-C5 has an ultra-low power and highly-integrated system with two processors:

- a high-performance 32-bit RISC-V processor (HP CPU), five-stage pipeline, clock frequency up to 240 MHz.
- a low-power 32-bit RISC-V processor (LP CPU), two-stage pipeline, clock frequency up to 40 MHz or 48 MHz (See the note below).

Note:
ESP32-C5 supports selection of crystal frequencies. see Chapter 9 Reset and Clock.

All internal memory, external memory, and peripherals are located on the HP CPU and LP CPU buses.

6.2 Features

• Address Space
    - 720 KB of internal memory address space, accessible by the instruction bus or data bus
    - 832 KB of peripheral address space
    - 32 MB of virtual address space for external memory, accessible by the instruction bus or data bus
    - 384 KB of internal DMA address space
    - 32 MB of external DMA address space

• Internal Memory
    - 320 KB of ROM
    - 384 KB of HP SRAM
    - 16 KB of LP SRAM

• External Memory
    - Up to 32 MB of external flash
    - Up to 32 MB of external RAM

• Peripheral Space
    - 61 modules/peripherals in total
```