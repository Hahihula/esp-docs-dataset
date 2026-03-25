

```markdown
Register 3.15. AHB_DMA_OUT_CONF1_CHn_REG (n: 0-1) (0x00D4+0xC0*n)

AHB_DMA_OUT_CHECK_OWNER_CHn Configures whether to enable owner bit check for TX channel n.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 3.16. AHB_DMA_OUT_PUSH_CHn_REG (n: 0-1) (0x00DC+0xC0*n)

AHB_DMA_OUTFIFO_WDATA_CHn Represents the data that need to be pushed into AHB DMA TX FIFO. (R/W)
AHB_DMA_OUTFIFO_PUSH_CHn Configures whether to push data into AHB DMA TX FIFO.
O: Invalid. No effect
1: Push
(WT)
```