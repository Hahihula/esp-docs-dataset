

```markdown
Chapter 21 Debug Assistant GoBack


## 21.3.2 SP Monitoring

The Debug Assistant module can monitor the SP so as to prevent stack overflow or erroneous push/pop in HP CPUO. When the HP CPUO SP goes below or beyond the lower or upper bound of the HP CPUO SP monitored region, the module will record the PC pointer and generate an interrupt. The bound is configured by software.

This is also the case for HP CPU1.


## 21.3.3 PC Logging

In some cases, software developers want to know the PC at the last reset of HP CPUO. For instance, when the program is stuck and can only be reset, the developer may want to know where the program got stuck in order to debug. The Debug Assistant module can record the PC at the last reset of HP CPUO, which can be then read for software debugging.

This is also the case for HP CPU1.


## 21.3.4 CPU/DMA Bus Access Logging

The Debug Assistant module can record the information about the HP CPUO Data bus's, HP CPU1 bus's, and DMA bus's write behaviors in real time. When a write operation occurs in or a specific value is written to a specified address space, the module will record the bus type, the address, PC (only when the write is performed by the HP CPUO or HP CPU1, will PC be recorded), and other information, and then store the data in the HP L2MEM in a certain format. The specified address range must fall within the permitted memory regions of HP SPM or HP L2MEM.


## 21.4 Interrupts

The following interrupt sources from the Debug Assistant module can generate the interrupt signal ASSIST_DEBUG_INT.

*   `ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_RD_INT`: Triggered when the HP CPUO Data bus reads in HP CPUO region 0.
*   `ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_WR_INT`: Triggered when the HP CPUO Data bus writes in HP CPUO region 0.
*   `ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_RD_INT`: Triggered when the HP CPUO Data bus reads in HP CPUO region 1.
*   `ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_WR_INT`: Triggered when the HP CPUO Data bus writes in HP CPUO region 1.
*   `ASSIST_DEBUG_CORE_O_AREA_PIF_O_RD_INT`: Triggered when the HP CPUO Peripheral bus reads in HP CPUO region 0.
*   `ASSIST_DEBUG_CORE_O_AREA_PIF_O_WR_INT`: Triggered when the HP CPUO Peripheral bus writes in HP CPUO region 0.
*   `ASSIST_DEBUG_CORE_O_AREA_PIF_1_RD_INT`: Triggered when the HP CPUO Peripheral bus reads in HP CPUO region 1.
```