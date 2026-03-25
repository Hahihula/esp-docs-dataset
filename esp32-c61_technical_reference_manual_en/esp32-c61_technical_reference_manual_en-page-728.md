

```markdown
| Name | Description | Address | Access |
|:---------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------|:-------|
| Bus logging configuration registers |  |  |  |
| MEM_MONITOR_LOG_SETTING_REG | Configures bus access logging | 0x0000 | R/W |
| MEM_MONITOR_LOG_SETTING1_REG | Configures bus access logging | 0x0004 | R/W |
| MEM_MONITOR_LOG_CHECK_DATA_REG | Configures data to be monitored for bus access logging | 0x0008 | R/W |
| MEM_MONITOR_LOG_DATA_MASK_REG | Configures data mask for bus access logging | 0x000C | R/W |
| MEM_MONITOR_LOG_MIN_REG | Configures the monitored lower address for bus access logging | 0x0010 | R/W |
| MEM_MONITOR_LOG_MAX_REG | Configures the monitored upper address for bus access logging | 0x0014 | R/W |
| MEM_MONITOR_LOG_MON_ADDR_UPDATE_O_REG | Configures whether to update the monitored address space for HP CPU bus access logging | 0x0018 | WT |
| MEM_MONITOR_LOG_MON_ADDR_UPDATE_1_REG | Configures whether to update the monitored address space for DMA_O bus access logging | 0x001C | WT |
| MEM_MONITOR_LOG_MEM_START_REG | Configures the starting address of the storage memory for recorded data | 0x0020 | R/W |
| MEM_MONITOR_LOG_MEM_END_REG | Configures the end address of the storage memory for recorded data | 0x0024 | R/W |
| MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG | Represents the address for the next write | 0x0028 | RO |
| MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG | Updates the address for the next write with the starting address for the recorded data | 0x002C | WT |
| MEM_MONITOR_LOG_MEM_FULL_FLAG_REG | Represents logging buffer overflow status register | 0x0030 | varies |
| Clock gating control register |  |  |  |
| MEM_MONITOR_CLOCK_GATE_REG | Clock gating control register | 0x0034 | R/W |
| Version control register |  |  |  |
```