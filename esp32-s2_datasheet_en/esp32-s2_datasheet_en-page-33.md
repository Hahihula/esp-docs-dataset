**Title: Functional Description**

- **Subtitle:** ULP-FSM has the following features:
  - support for common instructions including arithmetic, jump, and program control instructions
  - support for on-board sensor measurement instructions
  - boot by the CPU, its dedicated timer, or RTC GPIO

Note that these two co-processors cannot work simultaneously.

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter ULP Coprocessor (ULP)](#).

---

**Title: DMA Controller**

**Subtitle:** ESP32-S2 includes a DMA controller that allows peripheral-to-memory and memory-to-memory data transfer at a high speed. It has the following features:

- AHB bus architecture
- Half-duplex and full-duplex mode
- Programmable length of data to be transferred in bytes
- INCR burst transfer when accessing internal RAM
- Access to an address space of 320 KB at most in internal RAM
- Access to an address space of 10.5 MB at most in external RAM
- High-speed data transfer using DMA

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter DMA Controller (DMA)](#).

---

**Title: Memory Organization**

This subsection describes the memory arrangement to explain how data is stored, accessed, and managed for efficient operation.

Figure 4 illustrates the address mapping structure of ESP32-S2. 

[Image reference: Figure 4]

---

*Footer:*  
Espressif Systems  
ESP32-S2 Series Datasheet v1.8

*Link:* Submit Documentation Feedback