**Title: Chapter 3 System and Memory**

- **Supports up to 8 MB off-Chip SPI SRAM**
  - Peripherals
    - 41 peripherals
  - DMA
    - 13 modules are capable of DMA operation

The block diagram in Figure 3.2-1 illustrates the system structure, and the block diagram in Figure 3.2-2 illustrates the address map structure.

**Figure Caption:**
- **Figure 3.2-1 System Structure**

**Diagram Description (from left to right):**
- PRO_CPU
  - DMA -> Embedded Memory -> Cache -> MMU -> External Memory -> Peripheral
- APP_CPU

**Footer Information:**
- Espressif Systems
- ESP32 TRM (Version 5.6)
- Submit Documentation Feedback