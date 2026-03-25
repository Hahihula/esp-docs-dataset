

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)
```

## Chapter 17

### Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)

#### 17.1 Overview

Debug Assistant is an auxiliary module that features a set of functions to help locate bugs and issues during software debugging.

#### 17.2 Features

*   Read/write monitoring: Monitors whether the CPU bus reads from or writes to a specified memory address space. A detected read or write in the monitored address space will trigger an interrupt.
*   Stack pointer (SP) monitoring: Monitors whether the SP exceeds the specified address space. A bounds violation will trigger an interrupt.
*   Program counter (PC) logging: Records PC value. The developer can get the last PC value at the most recent CPU reset.
*   Bus access logging: Records the information about bus access. When the CPU or Direct Memory Access (DMA) controller writes a specified value, the Debug Assistant module will record the data type, address of this write operation, and additionally the PC value when the write is performed by the CPU, and push such information to the HP SRAM.

#### 17.3 Functional Description

##### 17.3.1 Region Read/Write Monitoring

The Debug Assistant module can monitor reads/writes performed by the CPU over data bus and peripheral bus in a certain address space, i.e., memory region. Whenever the bus reads or writes in the specified address space, an interrupt will be triggered. The data bus can monitor two memory regions (assuming they are region 0 and region 1, defined by developers' needs) at the same time, and so can Peripheral Bus.

##### 17.3.2 SP Monitoring

The Debug Assistant module can monitor the SP so as to prevent stack overflow or erroneous push/pop. When the SP exceeds the minimum or maximum threshold, the module will record the PC pointer and generate an interrupt. The threshold is configured by software.
```