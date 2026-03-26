

```markdown
| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 4   | HP_SYSTEM_RMT_MEM_CLK_FORCE_ON                                             |
| 3   | HP_SYSTEM_BITSCRAMBLER_TX_MEM_CLK_FORCE_ON                                 |
| 2   | HP_SYSTEM_BITSCRAMBLER_RX_MEM_CLK_FORCE_ON                                 |
| 1   | HP_SYSTEM_GDMA_MEM_CLK_FORCE_ON                                            |
| 0   | Reset                                                                      |

HP_SYSTEM_RMT_MEM_CLK_FORCE_ON Configures whether or not to force enable the clock gating of the memory clock in RMT.
- O: No effect
- 1: Force on (R/W)

HP_SYSTEM_BITSCRAMBLER_TX_MEM_CLK_FORCE_ON Configures whether or not to force enable the clock gating of the TX memory clock in BitScrambler.
- O: No effect
- 1: Force on (R/W)

HP_SYSTEM_BITSCRAMBLER_RX_MEM_CLK_FORCE_ON Configures whether or not to force enable the clock gating of the RX memory clock in BitScrambler.
- O: No effect
- 1: Force on (R/W)

HP_SYSTEM_GDMA_MEM_CLK_FORCE_ON Configures whether or not to force enable the clock gating of the memory clock in GDMA.
- O: No effect
- 1: Force on (R/W)
```