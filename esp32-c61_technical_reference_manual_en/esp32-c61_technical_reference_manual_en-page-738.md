

```markdown
Register 18.12. MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG (0x002C)

MEM_MONITOR_LOG_MEM_ADDR_UPDATE Configures whether to update the value in MEM_MONITOR_LOG_MEM_START_REG to the value of MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG.

O: Not update
1: Update
(WT)
```

```markdown
Register 18.13. MEM_MONITOR_LOG_MEM_FULL_FLAG_REG (0x0030)

MEM_MONITOR_LOG_MEM_FULL_FLAG Represents whether data overflows the storage space.

O: Not Overflow
1: Overflow
(RO)

MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG Configures whether to clear the-
MEM_MONITOR_LOG_MEM_FULL_FLAG flag bit.

O: Not clear (default)
1: Clear
(WT)
```