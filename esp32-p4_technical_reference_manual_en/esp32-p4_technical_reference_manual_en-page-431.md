

```markdown
| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 7   | DMA2D_OUT_RO_RAM_FORCE_PD_CHO              | Configures whether to force power down the macroblock reordering RAM for TX channel 0. <br> O: Not force power down <br> 1: Force power down <br> (R/W) |
| 6   | DMA2D_OUT_RO_RAM_FORCE_PU_CHO              | Configures whether to force power up the macroblock reordering RAM for TX channel 0. <br> O: Not force power up <br> 1: Force power up <br> (R/W) |
| 5   | DMA2D_OUT_RO_RAM_CLK_FO_CHO                | Configures the clock gating when TX channel 0 accessing the 2D-DMA RAM. <br> O: Use the clock gate <br> 1: Force the clock on and bypass the clock gate <br> (R/W) |
| 4   | (reserved)                                |                                                                             |
| 3   | (reserved)                                |                                                                             |
| 2   | (reserved)                                |                                                                             |
| 1   | (reserved)                                |                                                                             |
| 0   | Reset                                      |                                                                             |

Register 6.6. DMA2D_OUT_RO_PD_CONF_CHO_REG (0x0044)
```