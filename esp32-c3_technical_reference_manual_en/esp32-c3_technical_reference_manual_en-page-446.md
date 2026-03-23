

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG)
GoBack

Chapter 17

Debug Assistant (ASSIST_DEBUG)

17.1 Overview

Debug Assistant is an auxiliary module that features a set of functions to help locate bugs and issues during software debugging.

17.2 Features

* Read/write monitoring: Monitors whether the CPU bus has read from or written to a specified address space. A detected read or write will trigger an interrupt.
* Stack pointer (SP) monitoring: Monitors whether the SP exceeds the specified address space. A bounds violation will trigger an interrupt.
* Program counter (PC) logging: Records PC value. The developer can get the last PC value at the most recent CPU reset.
* Bus access logging: Records the information about bus access. When the CPU or DMA writes a specified value, the Debug Assistant module will record the address and PC value of this write operation, and push the data to the SRAM.

17.3 Functional Description

17.3.1 Region Read/Write Monitoring

The Debug Assistant module can monitor reads/writes performed by the CPU's Data bus and Peripheral bus in a certain address space, i.e., memory region. Whenever the Data bus reads or writes in the specified address space, an interrupt will be triggered. The Data bus can monitor two memory regions (assuming they are region 0 and region 1, defined by developer's needs) at the same time, so can the Peripheral bus.

17.3.2 SP Monitoring

The Debug Assistant module can monitor the SP so as to prevent stack overflow or erroneous push/pop. When the stack pointer exceeds the minimum or maximum threshold, Debug Assistant will record the PC pointer and generate an interrupt. The threshold is configured by software.
```