

```markdown
Chapter 3 System and Memory

## Chapter 3

### System and Memory

#### 3.1 Overview

The ESP32-C3 is an ultra-low-power and highly-integrated system with a 32-bit RISC-V single-core processor with a four-stage pipeline that operates at up to 160 MHz. All internal memory, external memory, and peripherals are located on the CPU buses.

#### 3.2 Features

*   **Address Space**
    -   792 KB of internal memory address space accessed from the instruction bus
    -   552 KB of internal memory address space accessed from the data bus
    -   836 KB of peripheral address space
    -   8 MB of external memory virtual address space accessed from the instruction bus
    -   8 MB of external memory virtual address space accessed from the data bus
    -   384 KB of internal DMA address space

*   **Internal Memory**
    -   384 KB of Internal ROM
    -   400 KB of Internal SRAM
    -   8 KB of RTC Memory

*   **External Memory**
    -   Supports up to 16 MB external flash

*   **Peripheral Space**
    -   35 modules/peripherals in total

*   **GDMA**
    -   7 GDMA-supported modules/peripherals

Figure 3.2-1 illustrates the system structure and address mapping.
```