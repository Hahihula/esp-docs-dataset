

```markdown
Register 4.24. AHB_DMA_TX_CRC_EN_ADDR_CHn_REG (n: 0-2) (0x02D0+0x28*n)

AHB_DMA_TX_CRC_EN_ADDR_CHn Configures at which bit of the CRC result the
AHB_DMA_TX_CRC_EN_WR_DATA_CHn_REG register targets for TX channel n. (R/W)

Register 4.25. AHB_DMA_TX_CRC_DATA_EN_WR_DATA_CHn_REG (n: 0-2) (0x02D4+0x28*n)

AHB_DMA_TX_CRC_DATA_EN_WR_DATA_CHn Configures whether to include each bit of the data
in the CRC calculation matrix for TX channel n.
O: Not include
1: Include
(R/W)
```