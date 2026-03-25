

```markdown
Chapter 20 Debug Assistant

Register 20.3. MEM_MONITOR_LOG_CHECK_DATA_REG (0x0008)

MEM_MONITOR_LOG_CHECK_DATA Configures the data to be monitored during bus accessing.
(R/W)

Register 20.4. MEM_MONITOR_LOG_DATA_MASK_REG (0x000C)

MEM_MONITOR_LOG_DATA_MASK Configures which byte(s) in MEM_MONITOR_LOG_CHECK_DATA_REG
to mask. Multiple bytes can be masked at the same time.

bit[0]: Configures whether to mask the least significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask

bit[1]: Configures whether to mask the second least significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask

bit[2]: Configures whether to mask the second most significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask

bit[3]: Configures whether to mask the most significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask
(R/W)
```