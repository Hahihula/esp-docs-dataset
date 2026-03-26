

# Chapter 21

## Debug Assistant

### 21.1 Overview

Debug Assistant is an auxiliary module that features a set of functions to help locate bugs and issues during software debugging.

### 21.2 Features

*   **Read/write monitoring:** Monitors whether the High-Performance dual-core CPU (HP CPU0 and HP CPU1) bus reads from or writes to a specified memory address space. A detected read or write in the monitored address space will trigger an interrupt.
*   **Stack pointer (SP) monitoring:** Monitors whether the SP exceeds the specified address space. A bounds violation will trigger an interrupt.
*   **Program counter (PC) logging:** Records the PC value. The developer can get the last PC value at the most recent reset of HP CPU0 or HP CPU1.
*   **Bus access logging:** Records the information about bus access. When the HP CPU0, HP CPU1, or the Direct Memory Access controller (DMA) writes a specified value, the Debug Assistant module will record the data type, address of this write operation, and additionally the PC value when the write is performed by HP CPU0 or HP CPU1, and push such information to the HP L2MEM.

### 21.3 Functional Description

#### 21.3.1 Region Read/Write Monitoring

The Debug Assistant module can monitor reads/writes performed by HP CPU0 bus in a certain address space, i.e., memory region. Whenever the bus reads or writes in the specified address space, an interrupt will be triggered. Please refer to Table 14-1 in Chapter 1 High-Performance CPU. In this chapter, when HP CPU0 bus accesses the data space, it is referred to as the Data bus, and when HP CPU0 bus accesses the AHB peripheral space, it is referred to as the Peripheral bus. The Data bus can monitor two memory regions (assuming they are HP CPU0 region 0 and HP CPU0 region 1, defined by developers' needs) at the same time, and so can Peripheral bus.

This is also the case for HP CPU1.