

```markdown
Register 22.10. AES_DMA_EXIT_REG (0x00B8)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| ... |                     |
| 1   | AES_DMA_EXIT        |
| 0   | Reset               |

AES_DMA_EXIT Configures whether to exit AES operation.
- 0: No effect
- 1: Exit
Only valid for DMA-AES operation. (WT)

Register 22.11. AES_PSEUDO_REG (0x00D0)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| ... |                              |
| 10  | AES_PSEUDO_RNG_CNT           |
| 9   | AES_PSEUDO_INC               |
| 7   | AES_PSEUDO_BASE              |
| 6   | AES_PSEUDO_EN                |
| 5-4  | (reserved)                   |
| 3   | Reset                       |

AES_PSEUDO_EN Configures whether to enable the pseudo-round function of AES.
- 0: Disabled
- 1: Enabled
(R/W)

AES_PSEUDO_BASE Configures the basic number of pseudo-rounds. (R/W)

AES_PSEUDO_INC Configures the random incremental number of pseudo-rounds. (R/W)

AES_PSEUDO_RNG_CNT Configures the frequency of pseudo-key updates in the pseudo-round function. (R/W)
```