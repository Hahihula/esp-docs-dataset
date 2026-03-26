

```markdown
Register 39.63. H264_DMA_OUT_RO_PD_CONF_CHO_REG (0x0044)

H264_DMA_OUT_RO_RAM_FORCE_PD_CHO Configures whether to force power down for DMA reorder RAM.
O: Not force power down
1: Force power down
(R/W)

H264_DMA_OUT_RO_RAM_FORCE_PU_CHO Configures whether to force power up for DMA reorder RAM.
O: Not force power up
1: Force power up
(R/W)

H264_DMA_OUT_RO_RAM_CLK_FO_CHO Configures whether to force enable clock gating for DMA TX reorder RAM.
O: A clock gating will be used when accessing the RAM in DMA
1: Force to open the clock and bypass the clock gating when accessing the RAM in DMA
(R/W)
```