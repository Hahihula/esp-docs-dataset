

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| L2_MEM_MONITOR_LOG_SETTING_REG            | Configures bus access logging                                              | 0x0000    | R/W    |
| L2_MEM_MONITOR_LOG_SETTING1_REG           | Configures bus access logging                                              | 0x0004    | R/W    |
| L2_MEM_MONITOR_LOG_CHECK_DATA_REG         | Configures monitored data in bus access logging                            | 0x0008    | R/W    |
| L2_MEM_MONITOR_LOG_DATA_MASK_REG          | Configures masked data in bus access logging                               | 0x000C    | R/W    |
| L2_MEM_MONITOR_LOG_MIN_REG                | Configures monitored address space in bus access logging                   | 0x0010    | R/W    |
| L2_MEM_MONITOR_LOG_MAX_REG                | Configures monitored address space in bus access logging                   | 0x0014    | R/W    |
| L2_MEM_MONITOR_LOG_MEM_START_REG          | Configures the starting address of the memory for recorded data             | 0x0018    | R/W    |
| L2_MEM_MONITOR_LOG_MEM_END_REG            | Configures the end address of the memory for recorded data                  | 0x001C    | R/W    |
| L2_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG   | Represents the address for the next write                                 | 0x0020    | RO     |
| L2_MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG    | Updates the address for the next write to the starting address for the recorded data | 0x0024    | WT     |
| L2_MEM_MONITOR_LOG_MEM_FULL_FLAG_REG      | Represents the logging overflow status                                     | 0x0028    | varies |
| Clock control register                    |                                                                             |           |        |
| L2_MEM_MONITOR_CLOCK_GATE_REG             | Clock control register                                                     | 0x002C     | R/W    |
| Version control register                  |                                                                             |           |        |
| L2_MEM_MONITOR_DATE_REG                   | Version control register                                                   | 0x03FC     | R/W    |

## 21.6.3 Summary of Other Registers

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Monitor configuration registers            |                                                                             |           |        |
| ASSIST_DEBUG_CORE_O_MONITOR_ENA_REG       | Configures whether to enable HP CPUO monitoring                            | 0x0000    | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MIN_REG  | Configures the lower bound address of region 0 monitored on HP              | 0x0010    | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_O_MAX_REG  | Configures the upper bound address of region 0 monitored on HP              | 0x0014    | R/W    |
| ASSIST_DEBUG_CORE_O_AREA_DRAMO_1_MIN_REG  | Configures the lower bound address of region 1 monitored on HP              | 0x0018    | R/W    |
```