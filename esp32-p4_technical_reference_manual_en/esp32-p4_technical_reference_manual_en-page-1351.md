

```markdown
Chapter 21 Debug Assistant

Register 21.3. SPM_MEM_MONITOR_LOG_DATA_MASK_REG (0x000C)

SPM_MEM_MONITOR_LOG_DATA_MASK   Configures which byte(s) in SPM_MEM_MONITOR_LOG_CHECK_DATA_REG to mask.
bit[0]:     Configures whether to mask the least significant byte of SPM_MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask

bit[1]:     Configures whether to mask the second least significant byte of SPM_MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask

bit[2]:     Configures whether to mask the second most significant byte of SPM_MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask

bit[3]:     Configures whether to mask the most significant byte of SPM_MEM_MONITOR_LOG_CHECK_DATA_REG.
    0: Not mask
    1: Mask
(R/W)

Register 21.4. SPM_MEM_MONITOR_LOG_MIN_REG (0x0010)

SPM_MEM_MONITOR_LOG_MIN   Configures the lower bound address of the monitored address space. (R/W)
```