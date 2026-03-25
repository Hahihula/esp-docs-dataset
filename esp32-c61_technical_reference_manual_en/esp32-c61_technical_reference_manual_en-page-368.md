

```markdown
Chapter 7 Reset and Clock

Register 7.43. PCR_PSram_MEM_MONITOR_CONF_REG (0x00CC)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 3   | POR_PSram_MEM_MONITOR_READY               | Represents whether or not PSRAM_MEM_MONITOR is released from reset.          |
| 2   | POR_PSram_MEM_MONITOR_RST_EN              | Configures whether or not to reset PSRAM_MEM_MONITOR.                        |
| 1   | PCR_PSram_MEM_MONITOR_CLK_EN              | Configures whether or not to enable PSRAM_MEM_MONITOR clock.                 |
| 0   | Reset                                     |                                                                             |

PCR_PSram_MEM_MONITOR_CLK_EN
Configures whether or not to enable PSRAM_MEM_MONITOR clock.
O: Not enable
1: Enable
(R/W)

PCR_PSram_MEM_MONITOR_RST_EN
Configures whether or not to reset PSRAM_MEM_MONITOR.
O: Not reset
1: Reset
(R/W)

PCR_PSram_MEM_MONITOR_READY
Represents whether or not PSRAM_MEM_MONITOR is released from reset.
O: Not released
1: Released
(RO)
```