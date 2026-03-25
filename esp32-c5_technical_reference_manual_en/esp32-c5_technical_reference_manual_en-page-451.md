

```markdown
Register 9.81. PCR_PSram_MEM_MONITOR_CONF_REG (0x0170)
```

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 3   | POR_PSram_MEM_MONITOR_READY                | Represents whether or not memory monitor of PSRAM is released from reset.<br>0: Not released<br>1: Released (RO) |
| 2   | PCR_PSram_MEM_MONITOR_RST_EN               | Configures whether to reset the memory monitor of PSRAM.<br>0: Not reset<br>1: Reset (R/W) |
| 1   | PCR_PSram_MEM_MONITOR_CLK_EN               | Configures whether to enable the PSRAM_MEM_MONITOR_CLK.<br>0: Not enable<br>1: Enable (R/W) |
| 0   | (reserved)                                |                                                                             |

```markdown
PCR_PSram_MEM_MONITOR_CLK_EN Configures whether to enable the PSRAM_MEM_MONITOR_CLK.
O: Not enable
1: Enable
(R/W)

PCR_PSram_MEM_MONITOR_RST_EN Configures whether to reset the memory monitor of PSRAM.
O: Not reset
1: Reset
(R/W)

PCR_PSram_MEM_MONITOR_READY Represents whether or not memory monitor of PSRAM is released from reset.
O: Not released
1: Released
(RO)
```