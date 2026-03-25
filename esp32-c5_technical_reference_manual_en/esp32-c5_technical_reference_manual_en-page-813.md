

```markdown
Chapter 20 Debug Assistant

GoBack

- Configure the HP CPU Peripheral bus region 1 with BUS_MONITOR_CORE_O_AREA_PIF_1_MIN_REG and BUS_MONITOR_CORE_O_AREA_PIF_1_MAX_REG.
- Configure the HP CPU SP bounds with BUS_MONITOR_CORE_O_SP_MIN_REG and BUS_MONITOR_CORE_O_SP_MAX_REG.

2. Configure BUS_MONITOR_CORE_O_INTR_ENA_REG to enable interrupts of a monitoring mode.

3. Configure BUS_MONITOR_CORE_O_MONTR_ENA_REG to enable the monitoring mode(s). Various monitoring modes can be enabled at the same time.

4. Read BUS_MONITOR_CORE_O_INTR_RAW_REG to get the raw interrupt status of a monitoring mode.

5. Configure BUS_MONITOR_CORE_O_INTR_CLR_REG to clear the interrupt of a monitoring mode.

For example, if the Debug Assistant module needs to monitor whether the HP CPU Data bus has written to [A ~ B] address space, the user can enable monitoring in either the HP CPU Data bus region 0 or region 1. The following configuration process is based on region 0:

1. Configure BUS_MONITOR_CORE_O_RCD_PDEBUGEN to 1 to enable HP CPU to update the PC signals to the Debug Assistant module.

2. Configure BUS_MONITOR_CORE_O_AREA_DRAMO_O_MIN_REG to Address A.

3. Configure BUS_MONITOR_CORE_O_AREA_DRAMO_O_MAX_REG to Address B.

4. Configure BUS_MONITOR_CORE_O_INTR_ENA_REG bit[1] to enable the interrupt for write operations by the HP CPU Data bus in region 0.

5. Configure BUS_MONITOR_CORE_O_MONTR_ENA_REG bit[1] to enable monitoring write operations by the HP CPU Data bus in region 0.

6. Configure interrupt matrix to map BUS_MONITOR_INTR into HP CPU interrupt (refer to Chapter 11 Interrupt Matrix).

7. After the interrupt is triggered:

- Read BUS_MONITOR_CORE_O_INTR_RAW_REG to identify the interrupt source.
- If the interrupt is triggered by HP CPU region monitoring, read BUS_MONITOR_CORE_O_AREA_PC for the HP CPU PC value, and BUS_MONITOR_CORE_O_AREA_SP for the HP CPU SP.
- If the interrupt is triggered by SP monitoring, read BUS_MONITOR_CORE_O_SP_PC for the HP CPU PC value.
- Write 1 to the corresponding bit of BUS_MONITOR_CORE_O_INTR_CLR_REG to clear the interrupt.

20.5.2 PC Logging Configuration

Configure BUS_MONITOR_CORE_O_RCD_PDEBUGEN to 1 to enable HP CPU to update the PC signals to the Debug Assistant module. If BUS_MONITOR_CORE_O_RCD_RECORDEN is also configured to 1, BUS_MONITOR_CORE_O_RCD_PDEBUGPC_REG will record the HP CPU’s PC value and BUS_MONITOR_CORE_O_RCD_PDEBUGSP_REG will record the HP CPU SP value. Otherwise, these two registers will retain their original values.

When the HP CPU resets, BUS_MONITOR_CORE_O_RCD_EN_REG will reset, while BUS_MONITOR_CORE_O_RCD_PDEBUGPC_REG and BUS_MONITOR_CORE_O_RCD_PDEBUGSP_REG will
```