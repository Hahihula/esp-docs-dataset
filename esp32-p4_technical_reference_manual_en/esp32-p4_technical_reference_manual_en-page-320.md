

```markdown
Register 4.94. AXI_DMA_OUT_CRC_INIT_DATA_CHn_REG (n: 0-2) (0x0180+0x68*n)

| 31 | 0 |
|----|---|
|    |   |
| Oxffffffff | Reset |

AXI_DMA_OUT_CRC_INIT_DATA_CHn Configures the CRC initial value for TX channel n. (R/W)


Register 4.95. AXI_DMA_TX_CRC_WIDTH_CHn_REG (n: 0-2) (0x0184+0x68*n)

| 31 | 3 | 2 | 1 | 0 |
|----|---|---|---|---|
|    |   |   |   | Reset |
| 0 | O | O | O | 0x0 |

AXI_DMA_TX_CRC_WIDTH_CHn Configures the CRC result width for TX channel n. O: ≤ 8 bits
1: ≤ 16 bits
2: ≤ 24 bits
3: ≤ 32 bits
(R/W)

AXI_DMA_TX_CRC_LAUNCH_FLGA_CHn Write 1 and then 0 to latch the values of AXI_DMA_TX_CRC_EN_ADDR_CHn, AXI_DMA_TX_CRC_DATA_EN_ADDR_CHn, AXI_DMA_TX_CRC_EN_WR_DATA_CHn, and AXI_DMA_TX_CRC_DATA_EN_WR_DATA_CHn. (R/W)
```