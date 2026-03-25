

```markdown
## 17.6.1 Bus Logging Configuration Registers

Register 17: MEM_MONITOR_LOG_SETTING_REG (0x0000)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 30  | Reset                                     |
| 29-8| (reserved)                                |
| 7   | MEM_MONITOR_LOG_MEM_LOOP_ENABLE           |
| 6   |                                            |
| 5   |                                            |
| 4   |                                            |
| 3   | MEM_MONITOR_LOG_MODE                      |
| 2   |                                            |
| 1   | MEM_MONITOR_LOG_ENA                       |
| 0   |                                            |

### MEM_MONITOR_LOG_ENA
Configures whether to enable CPU or DMA bus access logging.
- bit[0]: Configures whether to enable CPU bus access logging.
  - 0: Disable
  - 1: Enable
- bit[1]: Reserved
- bit[2]: Configures whether to enable DMA bus access logging.
  - 0: Disable
  - 1: Enable (R/W)

### MEM_MONITOR_LOG_MODE
Configures monitoring modes.
- bit[0]: Configures write monitoring.
  - 0: Disable
  - 1: Enable
- bit[1]: Configures word monitoring.
  - 0: Disable
  - 1: Enable
- bit[2]: Configures halfword monitoring.
  - 0: Disable
  - 1: Enable
- bit[3]: Configures byte monitoring.
  - 0: Disable
  - 1: Enable (R/W)

### MEM_MONITOR_LOG_MEM_LOOP_ENABLE
Configures the writing mode for the recorded data.
- 1: Loop mode
- 0: Non-loop mode (R/W)
```