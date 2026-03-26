

```markdown
Register 4.128. AXI_DMA_OUT_PRI_CHn_REG (n: 0-2) (0x0178+0x68*n)

AXI_DMA_TX_PRI_CHn   Configures the priority of RX channel n. The larger the value, the higher the priority.
Value range: 0 ~ 5. (R/W)

AXI_DMA_TX_CH_ARB_WEIGH_CHn   Configures the weight (i.e the number of tokens) of TX channel n.
Value range: 0 ~ 15. (R/W)

AXI_DMA_TX_ARB_WEIGH_OPT_DIR_CHn   Configures whether to enable weight optimization for RX channel n.
0: Enable
1: Disable
(R/W)

Register 4.129. AXI_DMA_IN_PERI_SEL_CHn_REG (n: 0-2) (0x0044+0x68*n)

AXI_DMA_PERI_IN_SEL_CHn   Configures the peripheral connected to RX channel n.
0: LCD_CAM
1: SPI2
2: SPI3
3: PARLIO
4: AES
5: SHA
6 ~ 15: Dummy-6 ~ Dummy-15
16 ~ 63: Invalid
(R/W)
```