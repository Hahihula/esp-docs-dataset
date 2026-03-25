

```markdown
Chapter 20 Debug Assistant

Register 20.7. MEM_MONITOR_LOG_MON_ADDR_UPDATE_O_REG (0x0018)

MEM_MONITOR_LOG_MON_ADDR_CORE_UPDATE Configures whether to update the monitored address space of the HP CPU bus as the address space from `MEM_MONITOR_LOG_MIN_REG` to `MEM_MONITOR_LOG_MAX_REG`.

O: Not update
1: Update

Other values: Invalid
(WT)

MEM_MONITOR_LOG_MON_ADDR_ALL_UPDATE Configures whether to update the monitored address space of all masters as the address space from `MEM_MONITOR_LOG_MIN_REG` to `MEM_MONITOR_LOG_MAX_REG`.

O: Not update
1: Update
(WT)
```