

```markdown
- Set the HP CPU SP bounds with BUS_MONITOR_CORE_O_SP_MIN_REG and BUS_MONITOR_CORE_O_SP_MAX_REG.
2. Set BUS_MONITOR_CORE_O_INTR_ENA_REG to enable interrupts for monitoring mode.
3. Set BUS_MONITOR_CORE_O_MONTR_ENA_REG to enable the monitoring mode(s). You can enable multiple monitoring modes simultaneously.
4. Read BUS_MONITOR_CORE_O_INTR_RAW_REG to obtain the raw interrupt status of a monitoring mode.
5. Set BUS_MONITOR_CORE_O_INTR_CLR_REG to clear the interrupt for a monitoring mode.

For example, if the Debug Assistant module needs to monitor whether the HP CPU Data bus has written to the [A ~ B] address space, the user can enable monitoring in either the HP CPU Data bus region 0 or region 1. The following configuration process is based on region 0:

1. Set BUS_MONITOR_CORE_O_RCD_PDEBUGEN to 1 to enable the HP CPU to update the PC signals to the Debug Assistant module.
2. Set BUS_MONITOR_CORE_O_AREA_DRAMO_O_MIN_REG to Address A.
3. Set BUS_MONITOR_CORE_O_AREA_DRAMO_O_MAX_REG to Address B.
4. Set BUS_MONITOR_CORE_O_INTR_ENA_REG bit[1] to enable the interrupt for write operations by the HP CPU Data bus in region 0.
5. Set BUS_MONITOR_CORE_O_MONTR_ENA_REG bit[1] to enable monitoring of write operations by the HP CPU Data bus in region 0.
6. Configure the interrupt matrix to map BUS_MONITOR_INTR into the HP CPU interrupt (refer to Chapter 9 Interrupt Matrix).
7. After the interrupt is triggered:
    - Read BUS_MONITOR_CORE_O_INTR_RAW_REG to identify the interrupt source.
    - If the interrupt is triggered by the HP CPU region monitoring, read BUS_MONITOR_CORE_O_AREA_PC for the HP CPU PC value and BUS_MONITOR_CORE_O_AREA_SP for the HP CPU SP.
    - If the interrupt is triggered by SP monitoring, read BUS_MONITOR_CORE_O_SP_PC for the HP CPU PC value.
    - Write 1 to the corresponding bit of BUS_MONITOR_CORE_O_INTR_CLR_REG to clear the interrupt.

## 18.5.2 PC Logging Configuration

Configure BUS_MONITOR_CORE_O_RCD_PDEBUGEN to 1 to enable the HP CPU to update the PC signals to the Debug Assistant module. If BUS_MONITOR_CORE_O_RCD_RECORDERN is also set to 1, BUS_MONITOR_CORE_O_RCD_PDEBUGPC_REG will record the HP CPU's PC value, and BUS_MONITOR_CORE_O_RCD_PDEBUGSP_REG will record the HP CPU's SP value. Otherwise, these two registers will retain their original values.

When the HP CPU resets, BUS_MONITOR_CORE_O_RCD_EN_REG will reset, while BUS_MONITOR_CORE_O_RCD_PDEBUGPC_REG and BUS_MONITOR_CORE_O_RCD_PDEBUGSP_REG will not. Therefore, these two registers will retain the PC and SP values during the HP CPU reset.
```