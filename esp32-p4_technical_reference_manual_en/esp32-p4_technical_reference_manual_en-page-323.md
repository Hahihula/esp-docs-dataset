
```markdown
Register 4.100. AXI_DMA_TX_CRC_DATA_EN_WR_DATA_CHn_REG (n: 0-2) (0x0198+0x68*n)

AXI_DMA_TX_CRC_DATA_EN_WR_DATA_CHn Configures whether to include each bit of the input data in the CRC calculation matrix for TX channel n.
0: Not include
1: Include
(R/W)
```
```markdown
Register 4.101. AXI_DMA_TX_CRC_DATA_EN_ADDR_CHn_REG (n: 0-2) (0x019C+0x68*n)

AXI_DMA_TX_CRC_DATA_EN_ADDR_CHn Configures at which bit of the CRC result the AAXI_DMA_TX_CRC_DATA_EN_WR_DATA_CHn_REG register targets for TX channel n. (R/W)
```