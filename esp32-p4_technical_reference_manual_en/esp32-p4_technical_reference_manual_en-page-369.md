

```markdown
Chapter 5 VDMA Controller (VDMA)                                     GoBack


Register 5.3. DMAC_CFG0_REG (0x0010)


DMAC_DMAC_EN Configures whether to enable VDMA.
O: Disable
1: Enable
Note: If this field is cleared but a channel is still active, this field will still return 1. When hardware has terminated activity on all channels, this field will return 0.
(R/W)

DMAC_INT_EN Configures whether to enable global interrupt.
O: Disable
1: Enable
(R/W)
```