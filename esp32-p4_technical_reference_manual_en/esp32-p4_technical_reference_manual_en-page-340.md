

```markdown
Register 4.127. AXI_DMA_IN_PRI_CHn_REG (n: 0-2) (0x0040+0x68*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 9   | AXI_DMA_RX_ARB_WEIGH_OPT_DIR_CHn                                           |
| 8   | AXI_DMA_RX_CH_ARB_WEIGH_CHn                                                 |
| 7   | AXI_DMA_RX_PRI_CHn                                                           |
| 4   | Reset                                                                       |
| 3   | 0                                                                             |
| 2   | 0                                                                             |
| 1   | 0                                                                             |
| 0   | 0x0                                                                          |

AXI_DMA_RX_PRI_CHn Configures the priority of RX channel n. The larger the value, the higher the priority.
Value range: 0 ~ 5. (R/W)

AXI_DMA_RX_CH_ARB_WEIGH_CHn Configures the weight (i.e the number of tokens) of RX channel n.
Value range: 0 ~ 15. (R/W)

AXI_DMA_RX_ARB_WEIGH_OPT_DIR_CHn Configures whether to enable weight optimization for RX channel n.
0: Enable
1: Disable
(R/W)
```