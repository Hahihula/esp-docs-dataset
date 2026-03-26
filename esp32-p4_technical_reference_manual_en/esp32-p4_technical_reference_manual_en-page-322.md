

```markdown
Register 4.98. AXI_DMA_TX_CRC_EN_WR_DATA_CHn_REG (n: 0-2) (0x0190+0x68*n)

AXI_DMA_TX_CRC_EN_WR_DATA_CHn Configures whether to include each bit of the intermediate result in the CRC calculation matrix for TX channel n.
O: Not include
I: Include
(R/W)
```

```markdown
Register 4.99. AXI_DMA_TX_CRC_EN_ADDR_CHn_REG (n: 0-2) (0x0194+0x68*n)

AXI_DMA_TX_CRC_EN_ADDR_CHn Configures at which bit of the CRC result the AXI_DMA_TX_CRC_EN_WR_DATA_CHn_REG register targets for TX channel n. (R/W)
```