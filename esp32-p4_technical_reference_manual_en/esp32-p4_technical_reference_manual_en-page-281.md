

```markdown
Register 4.30. AHB_DMA_RX_CRC_WIDTH_CHn_REG (n: 0-2) (0x0338+0x28*n)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   |   | Reset |
|        |     |   |   |   | 0x0 |

AHB_DMA_RX_CRC_WIDTH_CHn Configures the CRC result width for RX channel n.

0: ≤ 8 bits
1: ≤ 16 bits
2: ≤ 24 bits
3: ≤ 32 bits
(R/W)

AHB_DMA_RX_CRC_LAUNCH_FLGA_CHn Write 1 and then 0 to latch the values of AHB_DMA_RX_CRC_EN_ADDR_CHn, AHB_DMA_RX_CRC_DATA_EN_ADDR_CHn, AHB_DMA_RX_CRC_EN_WR_DATA_CHn, and AHB_DMA_RX_CRC_DATA_EN_WR_DATA_CHn. (R/W)

Register 4.31. AHB_DMA_IN_CRC_CLEAR_CHn_REG (n: 0-2) (0x033C+0x28*n)

| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|        |     |   | Reset |
|        |     |   | 0x0 |

AHB_DMA_IN_CRC_CLEAR_CHn_REG Reserved. (R/W)
```