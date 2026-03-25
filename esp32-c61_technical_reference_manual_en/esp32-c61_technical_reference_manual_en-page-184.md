

```markdown
Register 3.17. AHB_DMA_OUT_LINK_CHn_REG (n: 0-1) (0x00E0+0xC0*n)

AHB_DMA_OUTLINK_STOP_CHn   Configures whether to stop TX channel n from transmitting data.
O: Invalid. No effect
1: Stop
(WT)

AHB_DMA_OUTLINK_START_CHn   Configures whether to enable TX channel n for data transfer.
O: Disable
1: Enable
(WT)

AHB_DMA_OUTLINK_RESTART_CHn  Configures whether to restart TX channel n for AHB DMA transfer.
O: Invalid. No effect
1: Restart
(WT)

AHB_DMA_OUTLINK_PARK_CHn     Represents the status of the transmit descriptor's FSM.
O: Running
1: Idle
(RO)
```

```markdown
Register 3.18. AHB_DMA_TX_CH_ARB_WEIGH_CHn_REG (n: 0-1) (0x02DC+0x28*n)

AHB_DMA_TX_CH_ARB_WEIGH_CHn   Configures the weight (i.e the number of tokens) of TX channel n.
Value range: 0 ~ 15. (R/W)
```