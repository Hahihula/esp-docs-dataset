

```markdown
## 9.5.2 CPU Interrupts

The ESP32-H2 implements its interrupt mechanism using an interrupt controller instead of standard RISC-V ISA. The CPU has 32 interrupts, numbered from 0 to 31. The interrupts numbered 0, 3, 4, and 7 are used by the CPU for core-local interrupts (CLINT), while the remaining 28 interrupts (numbered 1, 2, 5, 6, and 8 ~ 31) are available for use by the interrupt matrix.

Each CPU interrupt has the following properties:

*   Priority levels from 1 (lowest) to 15 (highest).
*   Configurable as level-triggered or edge-triggered.
*   Lower-priority interrupts maskable by setting interrupt threshold.

**Note:**
For detailed information about the functions and configuration procedure of CPU interrupts, see Chapter 1 ESP-RISC-V CPU > Section 1.6 Interrupt Controller. The configuration registers of CPU interrupts are listed in Section 9.6.2 Interrupt Priority Register Summary.

## 9.5.3 Assign Peripheral Interrupt Source to CPU Interrupt

In this section, the following terms are used to describe the operation of the interrupt matrix.

*   **SOURCE:** stands for a peripheral interrupt source in Table 9.5-1.
*   **INTMTX_COREO_SOURCE_INTR_MAP_REG:** stands for the interrupt source mapping register for a SOURCE.
*   Num_P: stands for the index of CPU interrupts which can be 1, 2, 5, 6, 8 ~ 31.
*   Interrupt_P: stands for the CPU interrupt numbered as Num_P.

### 9.5.3.1 Assign One SOURCE to CPU Interrupt

Setting the corresponding source mapping register INTMTX_COREO_SOURCE_INTR_MAP_REG of **SOURCE** to Num_P assigns this interrupt source to Interrupt_P.

### 9.5.3.2 Assign Multiple SOURCES to CPU Interrupt

Setting the corresponding source mapping register INTMTX_COREO_SOURCE_INTR_MAP_REG of each SOURCE to the same Num_P assigns multiple sources to the same Interrupt_P. Any of these sources can trigger CPU Interrupt_P. When an interrupt signal is generated, CPU should check the interrupt status registers to figure out which peripheral generated the interrupt. For more information, see Chapter 1 ESP-RISC-V CPU > Section 1.6 Interrupt Controller.

### 9.5.3.3 Unassign SOURCE

Writing 0 to the INTMTX_COREO_SOURCE_INTR_MAP_REG register disables the corresponding interrupt source.
```