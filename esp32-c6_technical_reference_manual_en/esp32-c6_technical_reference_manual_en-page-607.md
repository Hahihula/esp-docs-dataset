

```markdown
## 18.3.3 PC Logging

In some cases, software developers want to know the PC at the last HP CPU reset. For instance, when the program is stuck and can only be reset, the developer may want to know where the program got stuck in order to debug. The Debug Assistant module can record the PC at the last HP CPU reset, which can be then read for software debugging.

## 18.3.4 CPU/DMA Bus Access Logging

The Debug Assistant module can record the information about the HP CPU Data bus's, LP CPU bus's, and DMA bus's write behaviors in real time. When a write operation occurs in or a specific value is written to a specified address space, the module will record the bus type, the address, PC (only when the write is performed by the HP CPU will PC be recorded), and other information, and then store the data in the HP SRAM in a certain format.

## 18.4 Recommended Operation

### 18.4.1 Region Monitoring and SP Monitoring Configuration

The Debug Assistant module can monitor reads and writes performed by the HP CPU's Data bus and Peripheral bus. Two memory regions on each bus can be monitored at the same time. All the monitoring modes supported by the Debug Assistant module are listed below:

*   Monitoring of the read/write operations performed by Data bus
    -   Data bus reads in region 0
    -   Data bus writes in region 0
    -   Data bus reads in region 1
    -   Data bus writes in region 1

*   Monitoring of the read/write operations performed by Peripheral bus
    -   Peripheral bus reads in region 0
    -   Peripheral bus writes in region 0
    -   Peripheral bus reads in region 1
    -   Peripheral bus writes in region 1

*   Monitoring of exceeding the SP bounds
    -   SP exceeds the upper bound address
    -   SP exceeds the lower bound address

The configuration process for region monitoring and SP monitoring is as follows:

1.  Configure monitored region and SP threshold.
    *   Configure Data bus region 0 with `ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MIN_REG` and `ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MAX_REG`.
```