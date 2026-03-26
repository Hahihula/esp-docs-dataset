

```markdown
Register 4.20. AHB_DMA_TX_CRC_WIDTH_CHn_REG (n: 0-2) (0x02C0+0x28*n)

AHB_DMA_TX_CRC_WIDTH_CHn Configures the CRC result width for TX channel n.
1: ≤ 16 bits
2: ≤ 24 bits
3: ≤ 32 bits
(R/W)

AHB_DMA_TX_CRC_LAUNCH_FLGA_CHn Write 1 and then 0 to latch the values of AHB_DMA_TX_CRC_EN_ADDR_CHn, AHB_DMA_TX_CRC_DATA_EN_ADDR_CHn, AHB_DMA_TX_CRC_EN_WR_DATA_CHn, and AHB_DMA_TX_CRC_DATA_EN_WR_DATA_CHn.
(R/W)

Register 4.21. AHB_DMA_OUT_CRC_CLEAR_CHn_REG (n: 0-2) (0x02C4+0x28*n)

AHB_DMA_OUT_CRC_CLEAR_CHn_REG Reserved. (R/W)
```