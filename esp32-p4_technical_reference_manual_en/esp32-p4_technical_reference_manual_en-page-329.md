

```markdown
Register 4.111. AXI_DMA_MISC_CONF_REG (0x02A8)
```

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 5   | AXI_DMA_CLK_EN                 | Configures AXI DMA clock gating.                                           |
|     |                                | 0: Support clock only when the application writes registers.                |
|     |                                | 1: Always force the clock on for registers.                                 |
| (R/W)|                                |                                                                             |
| 4   | AXI_DMA_ARB_PRI_DIS            | Configures whether to disable the priority arbitration.                     |
|     |                                | 0: Enable                                                                   |
|     |                                | 1: Disable                                                                  |
| (R/W)|                                |                                                                             |
| 3   | AXI_DMA_AXIM_RST_WR_INTER      | Write 1 and then 0 to reset the internal AXI write FSM. (R/W)               |
| 2   | AXI_DMA_AXIM_RST_RD_INTER      | Write 1 and then 0 to reset the internal AXI read FSM. (R/W)                |
|     |                                |                                                                             |
```