

```markdown
- HP CPU Data bus reads from HP CPU region 0.
- HP CPU Data bus writes to HP CPU region 0.
- HP CPU Data bus reads from HP CPU region 1.
- HP CPU Data bus writes to HP CPU region 1.

• Monitoring read/write operations on the Peripheral bus:
    - HP CPU Peripheral bus reads from HP CPU region 0.
    - HP CPU Peripheral bus writes to HP CPU region 0.
    - HP CPU Peripheral bus reads from HP CPU region 1.
    - HP CPU Peripheral bus writes to HP CPU region 1.

## 18.3.2 SP Monitoring

The Debug Assistant module monitors the SP to prevent stack overflow or erroneous push/pop operations in the HP CPU. When the HP CPU SP exceeds the monitored region’s lower or upper bounds, the module records the PC and generates an interrupt. The bounds are configured by software.

The supported SP monitoring modes are:

• The HP CPU SP exceeds the upper bound of the monitored region.
• The HP CPU SP falls below the lower bound of the monitored region.

## 18.3.3 PC Logging

Software developers may need to identify the PC value at the last reset of the HP CPU. For instance, when the program is stuck and requires a reset, the developer may want to know where the program got stuck to debug. The Debug Assistant module records the PC at the last reset of the HP CPU, which can then be read for debugging.

## 18.3.4 CPU/DMA Bus Access Logging

The Debug Assistant module records write operations of the HP CPU Data bus and the DMA bus in real time. When a write operation occurs or a specific value is written to a specified address space, the module records the bus type, address, PC (only when the write is performed by the HP CPU), and other information. It then stores the data in the HP SRAM in a specific format. The specified address range must fall within the permitted memory regions of HP SRAM or external RAM.

## 18.4 Interrupts

The Debug Assistant can generate the BUS_MONITOR_INT interrupt signal that will be sent to the **Interrupt Matrix**. The following interrupt sources can generate this interrupt signal.

• BUS_MONITOR_CORE_O_AREA_DRAMO_O_RD_INT: Triggered when the HP CPU Data bus reads from HP CPU region 0.
```