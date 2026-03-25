

```markdown
Chapter 20 Debug Assistant

GoBack

Chapter 20

Debug Assistant

20.1 Overview

Debug Assistant is an auxiliary module that features a set of functions to help locate bugs and issues during software debugging.

20.2 Features

The Debug Assistant module has the following features:

*   Region read/write monitoring: Monitors whether the High-Performance CPU (HP CPU) bus reads from or writes to a specified memory address space. A detected read or write in the monitored address space will trigger an interrupt.
*   Stack pointer (SP) monitoring: Monitors whether the SP exceeds the specified address space. A bounds violation will trigger an interrupt.
*   Program counter (PC) logging: Records the PC value. The last PC value at the most recent reset of HP CPU can be fetched.
*   Bus access logging: Records the information about bus access. When the HP CPU, Low-Power CPU (LP CPU), or the Direct Memory Access controller (DMA) writes a specified value, the Debug Assistant module will record the data type, address of this write operation, and additionally the PC value when the write is performed by HP CPU, and push such information to the HP SRAM.

20.3 Functional Description

20.3.1 Region Read/Write Monitoring

The Debug Assistant module can monitor reads/writes performed by HP CPU bus in a certain address space, i.e., memory region. Whenever the bus reads or writes to the specified address space, an interrupt will be triggered. Please refer to Table 2.4-1 in Chapter 2 High-Performance CPU.

In this chapter, when HP CPU bus accesses the data space, it is referred to as the Data bus, and when HP CPU bus accesses the AHB peripheral space, it is referred to as the Peripheral bus. The Debug Assistant module can simultaneously monitor two memory regions (assuming they are HP CPU region 0 and HP CPU region 1) on the Data bus, as well as on the Peripheral bus. The region 0 and 1 should be defined based on the developer’s needs. The supported region read/write monitoring modes are listed below.

*   Monitoring the read/write operations performed by the Data bus
```