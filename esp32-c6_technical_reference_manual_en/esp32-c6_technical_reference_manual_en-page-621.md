

```markdown
Register 18.9. MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG (0x0020)

MEM_MONITOR_LOG_MEM_ADDR_UPDATE Configures whether to update the value in  
MEM_MONITOR_LOG_MEM_START_REG to  
MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG.

1: Update  
0: Not update (default)  
(R/W)
```

```markdown
Register 18.10. MEM_MONITOR_LOG_MEM_FULL_FLAG_REG (0x0024)

MEM_MONITOR_LOG_MEM_FULL_FLAG Represents whether data overflows the storage space

0: Not Overflow  
1: Overflow  
(RO)

MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG Configures whether to clear the  
MEM_MONITOR_LOG_MEM_FULL_FLAG flag bit.

0: Not clear  
1: Clear  
(R/W)
```