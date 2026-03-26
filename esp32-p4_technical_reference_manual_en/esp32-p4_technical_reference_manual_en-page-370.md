

```markdown
Register 5.4. DMAC_CHENO_REG (0x0018)

DMAC_CHn_EN (n: 1-4) Configures whether to enable VDMA channel n. Hardware automatically clears this bit after the last AXI transfer of the DMA transfer has been completed. Software can poll this field to determine when this channel is free for a new DMA transfer.
0: Disable channel n
1: Enable channel n
(R/W)

DMAC_CHn_EN_WE (n: 1-4) Configures whether to enable write to DMAC_CHn_EN. This field always reads as O.
0: Disable write to DMAC_CHn_EN
1: Enable write to DMAC_CHn_EN
(WO)

DMAC_CHn_SUSP (n: 1-4) Configures whether to suspend channel n.
0: Do not suspend channel n
1: Suspend channel n
Software can clear this field to O after VDMA sets DMAC_CHn_CH_SUSPENDED_INTSTAT to 1, to exit the channel suspended mode.
Note: This field is cleared when channel n is disabled.
(R/W)

DMAC_CHn_SUSP_WE (n: 1-4) Configures whether to enable write to DMAC_CHn_SUSP. This field always reads as O.
0: Disable write to DMAC_CHn_SUSP
1: Enable write to DMAC_CHn_SUSP
(WO)
```