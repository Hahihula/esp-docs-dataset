
```markdown
Register 4.87. AXI_DMA_RX_CRC_DATA_EN_WR_DATA_CHn_REG (n: 0-2) (0x0060+0x68*n)

AXI_DMA_RX_CRC_DATA_EN_WR_DATA_CHn   Configures whether to include each bit of the data in the CRC calculation matrix for TX channel n.
0: Not Include
1: Include
(R/W)
```

```markdown
Register 4.88. AXI_DMA_RX_CRC_DATA_EN_ADDR_CHn_REG (n: 0-2) (0x0064+0x68*n)

AXI_DMA_RX_CRC_DATA_EN_ADDR_CHn   Configures at which bit of the CRC result the AXI_DMA_RX_CRC_DATA_EN_WR_DATA_CHn_REG register targets for TX channel n. (R/W)
```