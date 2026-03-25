

```markdown
Chapter 11 Interrupt Matrix

GoBack

11.5.2 HP CPU Interrupts

The HP CPU of the ESP32-C5 implements its interrupt mechanism using standard RISC-V (v0.9) Core-Local Interrupt Controller (CLIC) interrupt. The HP CPU supports 2 core local interrupts (CLINT) and 32 peripheral interrupts, which are numbered from 16 to 47. The peripheral interrupt sources are mapped to the 32 HP CPU peripheral interrupts through the interrupt matrix. Each HP CPU peripheral interrupt has the following properties:

*   Priority levels from 1 (lowest) to 15 (highest).
*   Configurable as level-triggered or edge-triggered.
*   Lower-priority interrupts maskable by setting interrupt threshold.

Note:
For detailed information about the functions and configuration procedures of CPU interrupts, see Chapter 2 High-Performance CPU > Section 2.8 Interrupt Controller. The configuration registers of CPU interrupts are listed in Section 11.6.2 Software Interrupt Register Summary.

11.5.3 Assign Peripheral Interrupt Source to HP CPU Peripheral Interrupt

In this section, the following terms are used to describe the operation of the interrupt matrix.

*   SOURCE: stands for a peripheral interrupt source in Table 11.5-1.
*   INTMTX_COREO_SOURCE_INTR_MAP_REG: stands for the interrupt source mapping register for a SOURCE.
*   Num_P: stands for the index of HP CPU interrupts which can be 16 ~ 47.
*   Interrupt_P: stands for the HP CPU interrupt numbered as Num_P.

11.5.3.1 Assign One Peripheral Interrupt Source to HP CPU Peripheral Interrupt

Setting the corresponding source mapping register INTMTX_COREO_SOURCE_INTR_MAP_REG of SOURCE to Num_P assigns this interrupt source to Interrupt_P.

11.5.3.2 Assign Multiple Peripheral Interrupt Sources to HP CPU Peripheral Interrupt

Setting the corresponding source mapping register INTMTX_COREO_SOURCE_INTR_MAP_REG of each SOURCE to the same Num_P assigns multiple sources to the same Interrupt_P. Any of these sources can trigger CPU Interrupt_P. When an interrupt signal is generated, the CPU should check the interrupt status registers to figure out which peripheral generated the interrupt. For more information, see Chapter 2 High-Performance CPU > Section 2.8 Interrupt Controller.

11.5.3.3 Unassign SOURCE

Writing 0 to the INTMTX_COREO_SOURCE_INTR_MAP_REG register disables the corresponding interrupt source.
```