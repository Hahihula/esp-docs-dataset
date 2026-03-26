

```markdown
Register 4.83. AXI_DMA_RX_CRC_WIDTH_CHn_REG (n: 0-2) (0x004C+0x68*n)

AXI_DMA_RX_CRC_WIDTH_CHn Configures the CRC result width for RX channel n.
0: ≤ 8 bits
1: ≤ 16 bits
2: ≤ 24 bits
3: ≤ 32 bits
(R/W)

AXI_DMA_RX_CRC_LAUNCH_FLGA_CHn Write 1 and then 0 to latch the values of AXI_DMA_RX_CRC_EN_ADDR_CHn, AXI_DMA_RX_CRC_DATA_EN_ADDR_CHn, AXI_DMA_RX_CRC_EN_WR_DATA_CHn, and AXI_DMA_RX_CRC_DATA_EN_WR_DATA_CHn.
(R/W)

Register 4.84. AXI_DMA_IN_CRC_CLEAR_CHn_REG (n: 0-2) (0x0050+0x68*n)

AXI_DMA_IN_CRC_CLEAR_CHn_REG Configures whether to clear the CRC result for RX channel n.
0: Not clear
1: Clear
(R/W)
```