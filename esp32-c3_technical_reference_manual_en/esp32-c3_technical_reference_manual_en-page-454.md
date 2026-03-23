

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| ASSIST_DEBUG_CORE_O_INTR_ENA_REG           | Interrupt enable register                                                   | 0x0008  | R/W    |
| ASSIST_DEBUG_CORE_O_INTR_CLR_REG           | Interrupt clear register                                                    | 0x000C  | R/W    |
| PC logging configuration register          |                                                                             |         |        |
| ASSIST_DEBUG_CORE_O_RCD_EN_REG             | PC logging enable register                                                  | 0x0044  | R/W    |
| PC logging status registers                |                                                                             |         |        |
| ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG       | PC logging register                                                         | 0x0048  | RO     |
| ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG       | PC logging register                                                         | 0x004C  | RO     |
| Bus access logging configuration registers |                                                                             |         |        |
| ASSIST_DEBUG_LOG_SETTING_REG               | Bus access logging configuration register                                   | 0x0070  | R/W    |
| ASSIST_DEBUG_LOG_DATA_O_REG                | Configures monitored data in Bus access logging                            | 0x0074  | R/W    |
| ASSIST_DEBUG_LOG_DATA_MASK_REG             | Configures masked data in Bus access logging                                | 0x0078  | R/W    |
| ASSIST_DEBUG_LOG_MIN_REG                   | Configures monitored address space in Bus access logging                    | 0x007C  | R/W    |
| ASSIST_DEBUG_LOG_MAX_REG                   | Configures monitored address space in Bus access logging                    | 0x0080  | R/W    |
| ASSIST_DEBUG_LOG_MEM_START_REG             | Configures the starting address of the storage memory for recorded data      | 0x0084  | R/W    |
| ASSIST_DEBUG_LOG_MEM_END_REG               | Configures the end address of the storage memory for recorded data           | 0x0088  | R/W    |
| ASSIST_DEBUG_LOG_MEM_CURRENT_ADDR_REG      | The current address of the storage memory for recorded data                  | 0x008C  | RO     |
| ASSIST_DEBUG_LOG_MEM_FULL_FLAG_REG         | Logging overflow status register                                           | 0x0090  | varies |
| CPU status registers                       |                                                                             |         |        |
| ASSIST_DEBUG_CORE_O_LASTPC_BEFORE_EXCEPTION_REG | PC of the last command before CPU enters exception                         | 0x0094  | RO     |
| ASSIST_DEBUG_CORE_O_DEBUG_MODE_REG         | CPU debug mode status register                                              | 0x0098  | RO     |
| Version register                           |                                                                             |         |        |
| ASSIST_DEBUG_DATE_REG                      | Version control register                                                    | 0x01FC  | R/W    |
```