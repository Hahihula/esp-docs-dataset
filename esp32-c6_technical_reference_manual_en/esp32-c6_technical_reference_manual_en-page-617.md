

```markdown
## 18.6.1 Bus Logging Configuration Registers

Register 18.1. MEM_MONITOR_LOG_SETTING_REG (0x0000)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 30  | O                                        |
| 29  | O                                        |
| ... | ...                                      |
| 8   | MEM_MONITOR_LOG_MEM_LOOP_ENABLE           |
| 7   |                                            |
| 6   |                                            |
| 5   |                                            |
| 4   |                                            |
| 3   | MEM_MONITOR_LOG_MODE                      |
| 2   | MEM_MONITOR_LOG_ENA                       |
| 1   | O                                        |
| 0   | Reset                                     |

MEM_MONITOR_LOG_ENA Configures whether to enable CPU or DMA bus access logging.
- bit[0]: Configures whether to enable HP CPU bus access logging.
  - 0: Disable
  - 1: Enable
- bit[1]: Configures whether to enable LP CPU bus access logging.
  - 0: Disable
  - 1: Enable
- bit[2]: Configures whether to enable DMA bus access logging.
  - 0: Disable
  - 1: Enable
  (R/W)

MEM_MONITOR_LOG_MODE Configures monitoring modes.
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
  - 1: Enable
  (R/W)

MEM_MONITOR_LOG_MEM_LOOP_ENABLE Configures the writing mode for recorded data.
- 1: Loop mode
- 0: Non-loop mode
  (R/W)
```