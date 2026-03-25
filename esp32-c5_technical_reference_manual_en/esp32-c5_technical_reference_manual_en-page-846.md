

```markdown
Chapter 20 Debug Assistant

Register 20.37. BUS_MONITOR_CORE_O_DEBUG_MODE_REG (0x0074)

BUS_MONITOR_CORE_O_DEBUG_MODE Represents whether RISC-V CPU (HP CPU) is in debugging mode.
1: In debugging mode
0: Not in debugging mode
(RO)

BUS_MONITOR_CORE_O_DEBUG_MODULE_ACTIVE Represents the status of the RISC-V CPU (HP CPU) debug module.
1: Active status
Other: Inactive status
(RO)

Register 20.38. BUS_MONITOR_CLOCK_GATE_REG (0x0108)

BUS_MONITOR_CLK_EN Configures whether to enable the register clock gating.
0: Disable
1: Enable
(R/W)
```