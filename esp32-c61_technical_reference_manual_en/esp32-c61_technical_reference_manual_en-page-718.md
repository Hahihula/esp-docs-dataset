

```markdown
Chapter 18 Debug Assistant

GoBack

Chapter 18

Debug Assistant

18.1 Overview

Debug Assistant is an auxiliary module that features a set of functions to help locate bugs and issues during software debugging.

18.2 Features

The Debug Assistant module has the following features:

* Region read/write monitoring: Monitors whether the High-Performance CPU (HP CPU) bus reads from or writes to a specified memory address space. A detected read or write in the monitored address space triggers an interrupt.
* Stack pointer (SP) monitoring: Monitors whether the SP exceeds the specified address space. A bounds violation triggers an interrupt.
* Program counter (PC) logging: Records the PC value. The last PC value at the most recent reset of the HP CPU can be retrieved.
* Bus access logging: Records information about bus access. When the HP CPU or the Direct Memory Access controller (DMA) writes a specified value, the Debug Assistant module records the data type, address of the write operation, and the PC value when the write is performed by the HP CPU, then stores this information in the HP SRAM.

18.3 Functional Description

18.3.1 Region Read/Write Monitoring

The Debug Assistant module monitors reads and writes performed by the HP CPU bus in a specified address space, i.e., memory region. Whenever the bus reads from or writes to this address space, an interrupt is triggered. Refer to Table 1.4-1 in Chapter 1 ESP-RISC-V CPU.

In this chapter, when the HP CPU bus accesses the data space, it is referred to as the Data bus. When the HP CPU bus accesses the AHB peripheral space, it is referred to as the Peripheral bus. The Debug Assistant module can simultaneously monitor two memory regions (HP CPU region 0 and HP CPU region 1) on the Data bus and the Peripheral bus. The regions should be defined based on the developer’s needs.

The supported region read/write monitoring modes are:

* Monitoring read/write operations on the Data bus:
```