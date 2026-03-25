

```markdown
Register 5.20. AHB_DMA_TX_ARB_WEIGH_OPT_DIR_CHn_REG (n: 0-2) (0x02E0+0x28*n)

AHB_DMA_TX_ARB_WEIGH_OPT_DIR_CHn   Configures whether to enable weight optimization for TX channel n.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 5.21. AHB_DMA_RX_CH_ARB_WEIGH_CHn_REG (n: 0-2) (0x0354+0x28*n)

AHB_DMA_RX_CH_ARB_WEIGH_CHn   Configures the weight (i.e. the number of tokens) of RX channel n.
Value range: 0 ~ 15. (R/W)
```