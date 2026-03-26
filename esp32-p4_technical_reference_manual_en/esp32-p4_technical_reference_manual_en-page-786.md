

```markdown
Chapter 12 Interrupt Matrix

GoBack

12.4.2 Assign Peripheral Interrupt Source to HP CPU Interrupt

In this section, the following terms are used to describe the operation of the interrupt matrix.
*   SOURCE: Stands for a peripheral interrupt source in Table 12.4-1.
*   COREx_SOURCE_MAP: Stands for an interrupt source mapping register for the peripheral interrupt source (SOURCE) of HP CPUx.
*   Num_P: The index of HP CPU interrupts, which can be 16 ~ 47.
*   Interrupt_P: Stands for the HP CPU interrupt numbered as Num_P.

12.4.2.1 Assign One Peripheral Interrupt Source (SOURCE) to HP CPUx

Setting the corresponding source mapping register COREx_SOURCE_MAP of SOURCE to Num_P assigns this interrupt source to Interrupt_P of HP CPUx.

12.4.2.2 Assign Multiple Peripheral Interrupt Sources (SOURCE) to HP CPUx

Setting the corresponding source mapping register COREx_SOURCE_MAP of each interrupt source to the same Num_P assigns multiple sources to the same Interrupt_P of HP CPUx. Any of these sources can trigger CPU Interrupt_P of HP CPUx. In other words, the CPU Interrupt_P will be shared between these interrupt sources. When an interrupt signal is generated, HP CPUx should check the interrupt status registers to determine which peripheral generated the interrupt. For more information, see Chapter 1 High-Performance CPU.

12.4.2.3 Disable HP CPUx Peripheral Interrupt Source (SOURCE)

Writing 0 to the COREx_SOURCE_MAP register disables the corresponding interrupt source.

12.4.3 Query Current Interrupt Status of HP CPUx Peripheral Interrupt Source

After enabling peripheral interrupt sources, users can query the current interrupt status of HP CPUx peripheral interrupt sources by reading the bit value in COREx_INTR_STATUS_n (read only). For the mapping between COREx_INTR_STATUS_n and peripheral interrupt sources, please refer to Table 12.4-1.

12.4.4 Interrupt Remapping

The RISC-V HP CPUx (x can be 0 or 1) of ESP32-P4 supports Machine Mode and User Mode.
HP CPUx provides a total of 32 peripheral interrupts. Each peripheral interrupt can be delegated by HP CPUx as either a Machine-mode interrupt or a User-mode interrupt.
Under normal conditions, when HP CPUx is running in Machine Mode, it can respond only to Machine-mode interrupts and cannot respond to User-mode interrupts. When HP CPUx is running in User Mode, it can respond to both Machine-mode and User-mode interrupts.
To allow HP CPUx to indirectly respond to User-mode interrupts while operating in Machine Mode, the system introduces the Interrupt Remap mechanism.

Espressif Systems
786
ESP32-P4 TRM
PRELIMINARY

Submit Documentation Feedback
```