

```markdown
Register 6.22. DMA2D_IN_RO_PD_CONF_CHO_REG (0x0548)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 7   | DMA2D_IN_RO_RAM_CLK_FO_CHO     | Configures the clock gating when RX channel 0 accessing the 2D-DMA RAM.      |
| 6   | DMA2D_IN_RO_RAM_FORCE_PU_CHO   | Configures whether to force power up the macroblock reordering RAM for RX channel 0.<br>0: Not force power up<br>1: Force power up (R/W) |
| 5   | DMA2D_IN_RO_RAM_FORCE_PD_CHO   | Configures whether to force power down the macroblock reordering RAM for RX channel 0.<br>0: Not force power down<br>1: Force power down (R/W) |
| 4   |                                | (reserved)                                                                  |
| 3   | DMA2D_IN_RO_RAM_FORCE_PU_CHO   | Configures whether to force power up the macroblock reordering RAM for RX channel 0.<br>0: Not force power up<br>1: Force power up (R/W) |
| 2   |                                | (reserved)                                                                  |
| 1   | DMA2D_IN_RO_RAM_FORCE_PD_CHO   | Configures whether to force power down the macroblock reordering RAM for RX channel 0.<br>0: Not force power down<br>1: Force power down (R/W) |
| 0   |                                | Reset                                                                       |

DMA2D_IN_RO_RAM_FORCE_PD_CHO Configures whether to force power down the macroblock reordering RAM for RX channel 0.
0: Not force power down
1: Force power down
(R/W)

DMA2D_IN_RO_RAM_FORCE_PU_CHO Configures whether to force power up the macroblock reordering RAM for RX channel 0.
0: Not force power up
1: Force power up
(R/W)

DMA2D_IN_RO_RAM_CLK_FO_CHO Configures the clock gating when RX channel 0 accessing the 2D-DMA RAM.
0: Use the clock gate
1: Force the clock on and bypass the clock gate
(R/W)
```