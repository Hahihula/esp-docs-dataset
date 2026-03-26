

```markdown
Register 4.130. AXI_DMA_OUT_PERI_SEL_CHn_REG (n: 0-2) (0x017C+0x68*n)

AXI_DMA_PERI_OUT_SEL_CHn Configures the peripheral connected to TX channel n.

O: LCD_CAM
1: SPI2
2: SPI3
3: PARLIO
4: AES
5: SHA
6 ~ 15: Dummy-6 ~ Dummy-15
16 ~ 63: Invalid

(R/W)

Register 4.131. AXI_DMA_RX_CRC_EN_WR_DATA_CHn_REG (n: 0-2) (0x0058+0x68*n)

AXI_DMA_RX_CRC_EN_WR_DATA_CHn Configures whether to include each bit of the intermediate result in the CRC calculation matrix for RX channel n.

O: Not include
1: Include

(R/W)
```