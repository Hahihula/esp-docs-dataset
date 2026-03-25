

```markdown
Register 5.18. AHB_DMA_OUT_LINK_CHn_REG (n: 0-2) (0x0E0+0xCO*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 4   | 3   | 2   | 1   | 0    | Reset                     |
|     | AHB_DMA_OUTLINK_PARK_CHn | AHB_DMA_OUTLINK_RESTART_CHn | AHB_DMA_OUTLINK_START_CHn | AHB_DMA_OUTLINK_STOP_CHn |

AHB_DMA_OUTLINK_STOP_CHn Configures whether to stop TX channel n from transmitting data.
- 0: Invalid. No effect
- 1: Stop (WT)

AHB_DMA_OUTLINK_START_CHn Configures whether to enable TX channel n for data transfer.
- 0: Disable
- 1: Enable (WT)

AHB_DMA_OUTLINK_RESTART_CHn Configures whether to restart TX channel n for AHB DMA transfer.
- 0: Invalid. No effect
- 1: Restart (WT)

AHB_DMA_OUTLINK_PARK_CHn Represents the status of the transmit descriptor’s FSM.
- 0: Running
- 1: Idle (RO)

Register 5.19. AHB_DMA_TX_CH_ARB_WEIGH_CHn_REG (n: 0-2) (0x02DC+0x28*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 4   | 3   | 0    | Reset                     |
|     | AHB_DMA_TX_CH_ARB_WEIGH_CHn |

AHB_DMA_TX_CH_ARB_WEIGH_CHn Configures the weight (i.e the number of tokens) of TX channel n.
Value range: 0 ~ 15. (R/W)
```