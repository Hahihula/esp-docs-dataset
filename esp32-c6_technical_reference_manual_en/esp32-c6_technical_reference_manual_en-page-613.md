

```markdown
| Name | Description | Address | Access |
|:---------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------|:-------|
| Bus access logging configuration registers | | | |
| MEM_MONITOR_LOG_SETTING_REG | Bus access logging configuration register | 0x0000 | R/W |
| MEM_MONITOR_LOG_CHECK_DATA_REG | Configures monitored data in Bus access logging | 0x0004 | R/W |
| MEM_MONITOR_LOG_DATA_MASK_REG | Configures masked data in Bus access logging | 0x0008 | R/W |
| MEM_MONITOR_LOG_MIN_REG | Configures monitored address space in Bus access logging | 0x000C | R/W |
| MEM_MONITOR_LOG_MAX_REG | Configures monitored address space in Bus access logging | 0x0010 | R/W |
| MEM_MONITOR_LOG_MEM_START_REG | Configures the starting address of the storage memory for recorded data | 0x0014 | R/W |
| MEM_MONITOR_LOG_MEM_END_REG | Configures the end address of the storage memory for recorded data | 0x0018 | R/W |
| MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG | Represents the address for the next write | 0x001C | RO |
| MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG | Updates the address for the next write with the starting address for the recorded data | 0x0020 | R/W |
| MEM_MONITOR_LOG_MEM_FULL_FLAG_REG | Logging overflow status register | 0x0024 | varies |
| Clock control register | | | |
| MEM_MONITOR_CLOCK_GATE_REG | Register clock control | 0x0028 | R/W |
| Version control register | | | |
| MEM_MONITOR_DATE_REG | Version control register | 0x03FC | R/W |

```