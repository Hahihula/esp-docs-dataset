

```markdown
Register 18.33. BUS_MONITOR_CORE_O_RCD_EN_REG (0x0044)

BUS_MONITOR_CORE_O_RCD_RECORDEN Configures whether to enable PC and SP logging.
O: Disable
1: BUS_MONITOR_CORE_O_RCD_PDEBUGPC_REG starts to record PC in real time,
   BUS_MONITOR_CORE_O_RCD_PDEBUGSP_REG starts to record SP in real time
   (R/W)

BUS_MONITOR_CORE_O_RCD_PDEBUGEN Configures whether to enable HP CPU debugging.
O: Disable
1: HP CPU outputs PC
   (R/W)

Register 18.34. BUS_MONITOR_CORE_O_RCD_PDEBUGPC_REG (0x0048)

BUS_MONITOR_CORE_O_RCD_PDEBUGPC Represents the PC value at HP CPU reset. (RO)
```