

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)
GoBack

Register 17.2. MEM_MONITOR_LOG_CHECK_DATA_REG (0x0004)

MEM_MONITOR_LOG_CHECK_DATA Configures the data to be monitored during bus accessing.
(R/W)

Register 17.3. MEM_MONITOR_LOG_DATA_MASK_REG (0x0008)

MEM_MONITOR_LOG_DATA_MASK Configures which byte(s) in
MEM_MONITOR_LOG_CHECK_DATA_REG to mask.

bit[0]: Configures whether to mask the least significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask

bit[1]: Configures whether to mask the second least significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask

bit[2]: Configures whether to mask the second most significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask

bit[3]: Configures whether to mask the most significant byte of
MEM_MONITOR_LOG_CHECK_DATA_REG.
O: Not mask
1: Mask
(R/W)
```