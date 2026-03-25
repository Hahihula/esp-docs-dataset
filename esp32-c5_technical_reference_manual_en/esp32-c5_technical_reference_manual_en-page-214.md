

```markdown
Register 5.12. AHB_DMA_IN_CONF1_CHn_REG (n: 0-2) (0x0074+0xC0*n)

AHB_DMA_IN_CHECK_OWNER_CHn   Configures whether to enable owner bit check for RX channel n.
    O: Disable
    1: Enable
(R/W)
```

```markdown
Register 5.13. AHB_DMA_IN_POP_CHn_REG (n: 0-2) (0x007C+0xC0*n)

AHB_DMA_INFIFO_RDATA_CHn   Represents the data popped from AHB DMA RX FIFO. (RO)
AHB_DMA_INFIFO_POP_CHn     Configures whether to pop data from AHB DMA RX FIFO.
    O: Invalid. No effect
    1: Pop
(WT)
```