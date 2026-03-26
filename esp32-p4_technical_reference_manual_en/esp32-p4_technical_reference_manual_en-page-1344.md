

```markdown
## 21.6 Register Summary

The addresses of HP CPU bus logging configuration registers (see 21.6.1) in this section are relative to the SPM Monitor base address. The addresses of DMA bus logging configuration registers (see 21.6.2) in this section are relative to the L2MEM Monitor base address. The addresses of other registers (see 21.6.3) are relative to the Bus Monitor base address. All base addresses are provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

### 21.6.1 HP CPU Bus Logging Configuration Register Summary

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| HP CPU bus logging configuration registers | | | |
| SPM_MEM_MONITOR_LOG_SETTING_REG | Configures bus access logging | 0x0000 | R/W |
| SPM_MEM_MONITOR_LOG_CHECK_DATA_REG | Configures monitored data in bus access logging | 0x0008 | R/W |
| SPM_MEM_MONITOR_LOG_DATA_MASK_REG | Configures masked data in bus access logging | 0x000C | R/W |
| SPM_MEM_MONITOR_LOG_MIN_REG | Configures monitored address space in bus access logging | 0x0010 | R/W |
| SPM_MEM_MONITOR_LOG_MAX_REG | Configures monitored address space in bus access logging | 0x0014 | R/W |
| SPM_MEM_MONITOR_LOG_MEM_START_REG | Configures the starting address of the memory for recorded data | 0x0018 | R/W |
| SPM_MEM_MONITOR_LOG_MEM_END_REG | Configures the end address of the memory for recorded data | 0x001C | R/W |
| SPM_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG | Represents the address for the next write | 0x0020 | RO |
| SPM_MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG | Updates the address for the next write to the starting address for the recorded data | 0x0024 | WT |
| SPM_MEM_MONITOR_LOG_MEM_FULL_FLAG_REG | Represents the logging overflow status | 0x0028 | varies |
| Clock control register | | | |
| SPM_MEM_MONITOR_CLOCK_GATE_REG | Clock control register | 0x002C | R/W |
| Version control register | | | |
| SPM_MEM_MONITOR_DATE_REG | Version control register | 0x03FC | R/W |

### 21.6.2 DMA Bus Logging Configuration Register Summary

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| DMA bus logging configuration registers | | | |
```