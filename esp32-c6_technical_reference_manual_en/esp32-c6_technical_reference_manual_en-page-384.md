

```markdown
Chapter 10 Interrupt Matrix (INTMTX)
GoBack

10.3.2 CPU Interrupts

The ESP32-C6 implements its interrupt mechanism using an interrupt controller instead of RISC-V Privileged ISA specification. The CPU has 32 interrupts, numbered from 0 ~ 31. The interrupts numbered 0, 3, 4, and 7 are used by the CPU for core-local interrupts (CLINT), while the remaining 28 interrupts (numbered 1, 2, 5, 6, and 8 ~ 31) are available for use in the interrupt matrix.

Each CPU interrupt has the following properties:

- Priority levels from 1 (lowest) to 15 (highest).
- Configurable as level-triggered or edge-triggered.
- Lower-priority interrupts mask-able by setting interrupt threshold.

Note:
For detailed information about the function and configuration of CPU interrupts, see Chapter 1 High-Performance CPU.

10.3.3 Assign Peripheral Interrupt Source to CPU Interrupt

In this section, the following terms are used to describe the operation of the interrupt matrix.

- Source_X: stands for a peripheral interrupt source, wherein X means the number of this interrupt source in Table 10.3-1.
- INTMTX_COREO_SOURCE_X_INTR_MAP_REG: stands for an interrupt source mapping register for the peripheral interrupt source (Source_X).
- Num_P: the index of CPU interrupts which can be 1, 2, 5, 6, 8 ~ 31.
- Interrupt_P: stands for the CPU interrupt numbered as Num_P.

10.3.3.1 Assign One Peripheral Interrupt Source (Source_X) to CPU

Setting the corresponding source mapping register INTMTX_COREO_SOURCE_X_INTR_MAP_REG of Source_X to Num_P assigns this interrupt source to Interrupt_P.

10.3.3.2 Assign Multiple Peripheral Interrupt Sources (Source_X) to CPU

Setting the corresponding source mapping register INTMTX_COREO_SOURCE_X_INTR_MAP_REG of each interrupt source to the same Num_P assigns multiple sources to the same Interrupt_P. Any of these sources can trigger CPU Interrupt_P. When an interrupt signal is generated, CPU should check the interrupt status registers to figure out which peripheral generated the interrupt. For more information, see Chapter 1 High-Performance CPU.

10.3.3.3 Disable CPU Peripheral Interrupt Source (Source_X)

Writing 0 to the INTMTX_COREO_SOURCE_X_INTR_MAP_REG register disables the corresponding interrupt source.
```