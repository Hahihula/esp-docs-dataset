

```markdown
Register 4.10. AHB_DMA_MISC_CONF_REG (0x0064)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 3   | AHB_DMA_CLK_EN              | Configures AHB DMA clock gating.                                           |
|     |                             | 0: Support clock only when the application writes registers                  |
|     |                             | 1: Always force the clock on for registers                                  |
|     | (R/W)                       |                                                                             |
| 2   | AHB_DMA_ARB_PRI_DIS         | Configures whether to disable the priority arbitration.                     |
|     |                             | 0: Enable                                                                   |
|     |                             | 1: Disable                                                                  |
|     | (R/W)                       |                                                                             |
| 1   | AHB_DMA_AHBM_RST_INTER      | Write 1 and then 0 to reset the internal AHB FSM. (R/W)                     |
| 0   |                             | Reset                                                                       |

AHB_DMA_CLK_EN Configures AHB DMA clock gating.
0: Support clock only when the application writes registers
1: Always force the clock on for registers
(R/W)

AHB_DMA_ARB_PRI_DIS Configures whether to disable the priority arbitration.
0: Enable
1: Disable
(R/W)

AHB_DMA_AHBM_RST_INTER Write 1 and then 0 to reset the internal AHB FSM. (R/W)
```