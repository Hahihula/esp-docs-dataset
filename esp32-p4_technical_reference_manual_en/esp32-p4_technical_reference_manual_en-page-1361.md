

```markdown
Chapter 21 Debug Assistant

Register 21.23. L2_MEM_MONITOR_LOG_MEM_FULL_FLAG_REG (0x0028)

L2_MEM_MONITOR_LOG_MEM_FULL_FLAG Represents whether data overflows the storage space.
O: Not overflow
1: Overflow
(RO)

L2_MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG Configures whether to clear the L2_MEM_MONITOR_LOG_MEM_FULL_FLAG flag bit.
O: Not clear (default)
1: Clear
(WT)

Register 21.24. L2_MEM_MONITOR_CLOCK_GATE_REG (0x002C)

L2_MEM_MONITOR_CLK_EN Configures whether to enable the register clock gating.
O: Disable
1: Enable
(R/W)
```