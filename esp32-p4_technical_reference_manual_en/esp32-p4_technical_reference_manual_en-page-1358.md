

```markdown
Chapter 21 Debug Assistant

Register 21.16. L2_MEM_MONITOR_LOG_DATA_MASK_REG (0x000C)

(reserved)
L2_MEM_MONITOR_LOG_DATA_MASK

bit[0]: Configures whether to mask the least significant byte of L2_MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask

bit[1]: Configures whether to mask the second least significant byte of L2_MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask

bit[2]: Configures whether to mask the second most significant byte of L2_MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask

bit[3]: Configures whether to mask the most significant byte of L2_MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask (R/W)

Register 21.17. L2_MEM_MONITOR_LOG_MIN_REG (0x0010)

L2_MEM_MONITOR_LOG_MIN

Configures the lower bound address of the monitored address space. (R/W)
```