

```markdown
- HP CPU Data bus reads from HP CPU region 0
- HP CPU Data bus writes to HP CPU region 0
- HP CPU Data bus reads from HP CPU region 1
- HP CPU Data bus writes to HP CPU region 1
• Monitoring the read/write operations performed by the Peripheral bus
    - HP CPU Peripheral bus reads from HP CPU region 0
    - HP CPU Peripheral bus writes to HP CPU region 0
    - HP CPU Peripheral bus reads from HP CPU region 1
    - HP CPU Peripheral bus writes to HP CPU region 1

## 20.3.2 SP Monitoring

The Debug Assistant module can monitor the SP to prevent stack overflow or erroneous push/pop in HP CPU. When the HP CPU SP exceeds the monitored region's lower or upper bounds, the module will record the PC and generate an interrupt. The bound is configured by software.

The supported SP monitoring modes are listed below.
• HP CPU SP goes beyond the upper bound of the HP CPU SP monitored region
• HP CPU SP goes below the lower bound of the HP CPU SP monitored region

## 20.3.3 PC Logging

In some cases, software developers may need to identify the PC value at the last reset of HP CPU. For instance, when the program is stuck and requires a reset, the developer may want to know where the program got stuck in order to debug. The Debug Assistant module can record the PC at the last reset of HP CPU, which can be then read for software debugging.

## 20.3.4 CPU/DMA Bus Access Logging

The Debug Assistant module can record the write operations of the HP CPU Data bus, LP CPU bus, and DMA bus in real time. When a write operation occurs in or a specific value is written to a specified address space, the module will record the bus type, the address, PC (only when the write is performed by the HP CPU), and other information. It will then store the data in the HP SRAM in a certain format. The specified address range must fall within the permitted memory regions of HP SRAM or external RAM.

## 20.4 Interrupts

The Debug Assistant can generate the BUS_MONITOR_INT interrupt signal that will be sent to the **Interrupt Matrix**. The following interrupt sources can generate this interrupt signal.
• BUS_MONITOR_CORE_O_AREA_DRAMO_O_RD_INT: Triggered when the HP CPU Data bus reads from HP CPU region 0.
```