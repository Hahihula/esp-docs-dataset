

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| DMA2D_IN_STATE_CH1_REG                    | Represents the working status of the receive descriptor of RX channel 1                           | 0x0624  | RO     |
| DMA2D_IN_SUC_EOF_DES_ADDR_CH1_REG         | Represents the eceive descriptor address when EOF occurs on RX channel 1                         | 0x0628  | RO     |
| DMA2D_IN_ERR_EOF_DES_ADDR_CH1_REG         | Represents the receive descriptor address when errors occur on RX channel 1                     | 0x062C  | RO     |
| DMA2D_IN_DSCR_CH1_REG                     | Represents the address of the next receive descriptor pointed by the current pre-read receiver descriptor on RX channel 1 | 0x0630  | RO     |
| DMA2D_IN_DSCR_BFO_CH1_REG                 | Represents address of the current pre-read receive descriptor on RX channel 1                   | 0x0634  | RO     |
| DMA2D_IN_DSCR_BF1_CH1_REG                 | Represents the address of the previous pre-read receive descriptor on RX channel 1              | 0x0638  | RO     |
| DMA2D_AXI_ERR_REG                         | Represents the status of the AXI bus                                                             | 0x0A00  | RO     |
| DMA2D_DATE_REG                            | Version register                                                                                | 0x0A2C  | R/W    |
| Peripheral Select Registers               |                                                                                                  |         |        |
| DMA2D_OUT_PERI_SEL_CHO_REG                | Configures the peripheral connected to TX channel 0                                              | 0x0038  | R/W    |
| DMA2D_OUT_PERI_SEL_CH1_REG                | Configures the peripheral connected to TX channel 1                                              | 0x0138  | R/W    |
| DMA2D_OUT_PERI_SEL_CH2_REG                | Configures the peripheral connected to TX channel 2                                              | 0x0238  | R/W    |
| DMA2D_OUT_PERI_SEL_CH3_REG                | Configures the peripheral connected to TX channel 3                                              | 0x0338  | R/W    |
| DMA2D_IN_PERI_SEL_CHO_REG                 | Configures the peripheral connected to RX channel 0                                              | 0x053C  | R/W    |
| DMA2D_IN_PERI_SEL_CH1_REG                 | Configures the peripheral connected to RX channel 1                                              | 0x063C  | R/W    |
| DMA2D_IN_PERI_SEL_CH2_REG                 | Configures the peripheral connected to RX channel 2                                              | 0x073C  | R/W    |
```