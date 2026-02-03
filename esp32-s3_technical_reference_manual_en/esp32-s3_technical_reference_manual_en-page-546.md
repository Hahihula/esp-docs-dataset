Title: Chapter 9 Interrupt Matrix (INTERRUPT)

Section Title:
- GoBack

Subsection Titles and Body Text:

**9.3.3.2 Allocate multiple peripheral interrupt sources (Source_Yn) to CPUx**
Body Text:
Setting the corresponding configuration register `INTERRUPT_COREx_SOURCE_Yn_MAP_REG` of each interrupt source to the same Num_P allocates multiple sources to the same Interrupt_P. Any of these sources can trigger CPUx Interrupt_P. When an interrupt signal is generated, CPUx checks the interrupt status registers to figure out which peripheral the signal comes from.

**9.3.3.3 Disable CPUx peripheral interrupt source (Source_Y)**
Body Text:
Setting the corresponding configuration register `INTERRUPT_COREx_SOURCE_Y_MAP_REG` of the source to any Num_I disables this interrupt Source_Y. The choice of Num_I (6, 7, 11, 15, 16, 29) does not matter, as none of peripheral interrupt sources allocated to Num_I is connected to the CPUx. Therefore this functionality can be used to disable peripheral interrupt sources.

**9.3.4 Disable CPUx NMI Interrupt**
Body Text:
All CPUx interrupts, except for NMI interrupt (No.14 in Table 9.3-2), can be masked and enabled by software using CPU special register (INTENABLE). NMI interrupt cannot be masked by the way above, but ESP32-S3 provides two ways to mask NMI interrupt:
- Disconnect peripheral interrupt sources from NMI interrupt, i.e., the sources routed to NMI interrupt before are now routed to other interrupts. By such way, the previous NMI interrupt is maskable.
- Connect peripheral interrupt sources with NMI interrupt, but use World Controller module to mask NMI interrupt.

For more information, see Chapter 16 World Controller (WCL).

**9.3.5 Query Current Interrupt Status of Peripheral Interrupt Source**
Body Text:
Users can query current interrupt status of a CPUx peripheral interrupt source by reading the bit value in `INTERRUPT_COREx_INTR_STATUS_n_REG` (read only). For the mapping between `INTERRUPT_COREx_INTR_STATUS_n_REG` and peripheral interrupt sources, please refer to Table 9.3-1.

**9.4 Register Summary**
Body Text:
The addresses in this section are relative to the Interrupt Matrix base address provided in Table 4.3-3 in Chapter [4 System and Memory](#).

The abbreviations given in Column `Access` (read only) for registers.
The access types explained in Section Access Types.

Footer Information:

- Espressif Systems
- Page Number: 546
- Document Title: ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback