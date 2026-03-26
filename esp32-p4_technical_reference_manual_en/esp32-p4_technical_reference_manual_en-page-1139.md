

# Chapter 19

## Permission Control (PMS)

### 19.1 Overview

The permission control of ESP32-P4 consists of two parts: PMP (Physical Memory Protection) and APM (Access Permission Management).

PMP is located inside the HP CPUs and can control the HP CPUs' access to all address spaces. APM is an access permission management module located at the bus port, which can manage the permissions for the CPU (HP CPUO/1, LP CPU) to access the registers of all on-chip peripherals (see HP CPU PERI, HP PERI, and LP PERI in Table 19.1-1) and part of internal and external memory. The APM can also manage DMA masters like VDMA, USB OTG 2.0, to access parts of internal and external memory.

The APM module compares the configurable address range or the fixed address range, the access permissions of each address range, and the information carried on the bus like master ID, security mode, access address, access type, etc., to determine whether the access is allowed. With APM, users can precisely control the access of all masters to the memory and peripheral registers.

The distribution of management areas by PMP and APM is shown in Table 19.1-1. For HP CPUO/1, the control relationship between PMP and APM is shown in Figure 19.1-1.

Table 19.1-1. Management Areas by PMP and APM

| Slave | Master | HP CPUO | HP CPU1 | LP CPU | DMA Masters¹ |
| :------------------- | :------ | :------- | :-------- | :-------- | :------------ |
| HP ROM² | PMP | PMP | HP APM | DMA APM |
| HP SPM | PMP | PMP | N/A | N/A |
| HP L2MEM² | PMP | PMP | HP APM | DMA APM |
| EXT MEM² | PMP | PMP | HP APM | DMA APM |
| Direct Access HP ROM³ | PMP + HP APM | PMP + HP APM | N/A | N/A |
| Direct Access HP L2MEM³ | PMP + HP APM | PMP + HP APM | N/A | N/A |
| Direct Access EXT MEM³ | PMP + HP APM | PMP + HP APM | N/A | N/A |
| HP CPU PERI⁴ | PMP + HP APM | PMP + HP APM | HP APM | N/A |
| HP PERI⁵ | PMP + HP APM | PMP + HP APM | HP APM | N/A |
| LP PERI⁶ | PMP + LP APM | PMP + LP APM | LP APM | N/A |
| LP ROM | N/A | N/A | N/A | N/A |
| LP SRAM | PMP + LP APM | PMP + LP APM | N/A | N/A |

---

¹ DMA Masters refers to the set of DMA controllers managed by this permission scheme.
² These are typically internal memory regions protected at hardware level with PMP.
³ Direct access areas may require combined permissions from both CPU and APM for security enforcement.
⁴ HP CPU PERI: High-Performance CPU Peripheral Interface registers.
⁵ HP PERI: High-Performance Peripheral Interface (general on-chip peripherals).
⁶ LP PERI: Low-Power Peripheral Interface.

Espressif Systems
1139
ESP32-P4 TRM
PRELIMINARY