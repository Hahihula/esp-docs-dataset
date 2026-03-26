

```markdown
Register 4.78. AXI_DMA_IN_CONF1_CHn_REG (n: 0-2) (0x0014+0x68*n)

AXI_DMA_IN_CHECK_OWNER_CHn Configures whether to enable owner bit check for RX channel n.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 4.79. AXI_DMA_IN_POP_CHn_REG (n: 0-2) (0x0D1C+0x68*n)

AXI_DMA_INFIFO_RDATA_CHn Represents the data popped from AXI DMA RX FIFO. (RO)
AXI_DMA_INFIFO_POP_CHn Configures whether to pop data from AXI DMA RX FIFO.
O: Invalid. No effect
1: Pop
(WT)
```