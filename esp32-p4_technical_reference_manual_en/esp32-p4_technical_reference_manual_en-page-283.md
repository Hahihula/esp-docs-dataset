

```markdown
Register 4.34. AHB_DMA_RX_CRC_EN_ADDR_CHn_REG (n: 0-2) (0x0348+0x28*n)

AHB_DMA_RX_CRC_EN_ADDR_CHn Configures at which bit of the CRC result the AHB_DMA_RX_CRC_EN_WR_DATA_CHn_REG register targets for RX channel n. (R/W)
```

```markdown
Register 4.35. AHB_DMA_RX_CRC_DATA_EN_WR_DATA_CHn_REG (n: 0-2) (0x034C+0x28*n)

AHB_DMA_RX_CRC_DATA_EN_WR_DATA_CHn Configures whether to include each bit of the data in the CRC calculation matrix for RX channel n.
O: Not include
1: Include
(R/W)
```