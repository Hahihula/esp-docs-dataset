
```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AXI_DMA_RX_CRC_DATA_EN_ADDR_CH1_REG        | RX channel 1 CRC data input mask target register                                                | 0x00CC  | R/W    |
| AXI_DMA_IN_CONF0_CH2_REG                   | Configuration register 0 of RX channel 2                                                        | 0x00E0  | R/W    |
| AXI_DMA_IN_CONF1_CH2_REG                   | Configuration register 1 of RX channel 2                                                        | 0x00E4  | R/W    |
| AXI_DMA_IN_POP_CH2_REG                     | Pop control register of RX channel 2                                                           | 0x00EC  | varies |
| AXI_DMA_IN_LINK1_CH2_REG                   | Linked list descriptor configuration and control register 1 of RX channel 2                    | 0x00F0  | varies |
| AXI_DMA_IN_LINK2_CH2_REG                   | Linked list descriptor configuration and control register 2 of RX channel 2                    | 0x00F4  | R/W    |
| AXI_DMA_IN_CRC_INIT_DATA_CH2_REG           | RX channel 2 CRC initial value configuration register                                          | 0x0118  | R/W    |
| AXI_DMA_RX_CRC_WIDTH_CH2_REG               | RX channel 2 CRC result width configuration register                                           | 0x011C  | R/W    |
| AXI_DMA_IN_CRC_CLEAR_CH2_REG               | RX channel 2 CRC result clear register                                                         | 0x0120  | R/W    |
| AXI_DMA_IN_CRC_FINAL_RESULT_CH2_REG        | RX channel 2 CRC result register                                                               | 0x0124  | RO     |
| AXI_DMA_RX_CRC_EN_ADDR_CH2_REG             | RX channel 2 CRC intermediate result mask target register                                      | 0x012C  | R/W    |
| AXI_DMA_RX_CRC_DATA_EN_WR_DATA_CH2_REG     | CRC RX channel 2 CRC intermediate result mask register                                        | 0x0130  | R/W    |
| AXI_DMA_RX_CRC_DATA_EN_ADDR_CH2_REG        | RX channel 2 CRC data input mask target register                                                | 0x0134  | R/W    |
| AXI_DMA_OUT_CONF0_CHO_REG                  | Configuration register 0 of TX channel 0                                                       | 0x0148  | R/W    |
| AXI_DMA_OUT_CONF1_CHO_REG                  | Configuration register 1 of TX channel 0                                                      | 0x014C  | R/W    |
| AXI_DMA_OUT_PUSH_CHO_REG                   | Push control register of TX channel 0                                                         | 0x0154  | varies |
| AXI_DMA_OUT_LINK1_CHO_REG                  | Linked list descriptor configuration and control register 1 of TX channel 0                   | 0x0158  | varies |
| AXI_DMA_OUT_LINK2_CHO_REG                  | Linked list descriptor configuration and control register 2 of TX channel 0                   | 0x015C  | R/W    |
| AXI_DMA_OUT_CRC_INIT_DATA_CHO_REG          | TX channel 0 CRC initial value configuration register                                         | 0x0180  | R/W    |
| AXI_DMA_TX_CRC_WIDTH_CHO_REG               | TX channel 0 CRC result width configuration register                                          | 0x0184  | R/W    |
| AXI_DMA_OUT_CRC_CLEAR_CHO_REG              | TX channel 0 CRC result clear register                                                        | 0x0188  | R/W    |
| AXI_DMA_OUT_CRC_FINAL_RESULT_CHO_REG       | TX channel 0 CRC result register                                                              | 0x018C  | RO     |
| AXI_DMA_TX_CRC_EN_WR_DATA_CHO_REG          | CRC TX channel 0 CRC intermediate result mask register                                        | 0x0190  | R/W    |
| AXI_DMA_TX_CRC_EN_ADDR_CHO_REG             | TX channel 0 CRC intermediate result mask target register                                     | 0x0194  | R/W    |
| AXI_DMA_TX_CRC_DATA_EN_WR_DATA_CHO_REG     | TX channel 0 CRC data input mask register                                                     | 0x0198  | R/W    |
```