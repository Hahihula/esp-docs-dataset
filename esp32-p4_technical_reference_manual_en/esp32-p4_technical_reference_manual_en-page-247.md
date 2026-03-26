
```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_IN_POP_CH2_REG                    | Pop control register of RX channel 2                                                            | 0x01FC  | varies |
| AHB_DMA_IN_LINK_CH2_REG                   | Linked list descriptor configuration and control register of RX channel 2                        | 0x0200  | varies |
| AHB_DMA_OUT_CONFO_CH2_REG                 | Configuration register 0 of TX channel 2                                                       | 0x0250  | R/W    |
| AHB_DMA_OUT_CONF1_CH2_REG                 | Configuration register 1 of TX channel 2                                                      | 0x0254  | R/W    |
| AHB_DMA_OUT_PUSH_CH2_REG                  | Push control register of TX channel 2                                                          | 0x025C  | varies |
| AHB_DMA_OUT_LINK_CH2_REG                  | Linked list descriptor configuration and control register of TX channel 2                      | 0x0260  | varies |
| AHB_DMA_OUT_CRC_INIT_DATA_CHO_REG         | TX channel 0 CRC initial value configuration register                                          | 0x02BC  | R/W    |
| AHB_DMA_TX_CRC_WIDTH_CHO_REG              | TX channel 0 CRC result width configuration register                                          | 0x02C0  | R/W    |
| AHB_DMA_OUT_CRC_CLEAR_CHO_REG             | TX channel 0 CRC result clear register                                                        | 0x02C4  | R/W    |
| AHB_DMA_OUT_CRC_FINAL_RESULT_CHO_REG      | TX channel 0 CRC result register                                                              | 0x02C8  | RO     |
| AHB_DMA_TX_CRC_EN_WR_DATA_CHO_REG         | CRC TX channel 0 CRC intermediate result mask register                                        | 0x02CC  | R/W    |
| AHB_DMA_TX_CRC_EN_ADDR_CHO_REG            | TX channel 0 CRC intermediate result mask target register                                     | 0x02D0  | R/W    |
| AHB_DMA_TX_CRC_DATA_EN_WR_DATA_CHO_REG    | TX channel 0 CRC data input mask register                                                     | 0x02D4  | R/W    |
| AHB_DMA_TX_CRC_DATA_EN_ADDR_CHO_REG       | TX channel 0 CRC data input mask target register                                              | 0x02D8  | R/W    |
| AHB_DMA_TX_CH_ARB_WEIGH_CHO_REG           | TX channel 0 arbitration weight configuration register                                        | 0x02DC  | R/W    |
| AHB_DMA_TX_ARB_WEIGH_OPT_DIR_CHO_REG      | TX channel 0 weight arbitration optimization enable register                                 | 0x02E0  | R/W    |
| AHB_DMA_OUT_CRC_INIT_DATA_CH1_REG         | TX channel 1 CRC initial value configuration register                                         | 0x02E4  | R/W    |
| AHB_DMA_TX_CRC_WIDTH_CH1_REG              | TX channel 1 CRC result width configuration register                                          | 0x02E8  | R/W    |
| AHB_DMA_OUT_CRC_CLEAR_CH1_REG             | TX channel 1 CRC result clear register                                                        | 0x02EC  | R/W    |
| AHB_DMA_OUT_CRC_FINAL_RESULT_CH1_REG      | TX channel 1 CRC result register                                                              | 0x02F0  | RO     |
| AHB_DMA_TX_CRC_EN_WR_DATA_CH1_REG         | TX channel 1 CRC intermediate result mask register                                            | 0x02F4  | R/W    |
| AHB_DMA_TX_CRC_EN_ADDR_CH1_REG            | TX channel 1 CRC intermediate result mask target register                                    | 0x02F8  | R/W    |
| AHB_DMA_TX_CRC_DATA_EN_WR_DATA_CH1_REG    | TX channel 1 CRC data input mask register                                                     | 0x02FC  | R/W    |
| AHB_DMA_TX_CRC_DATA_EN_ADDR_CH1_REG       | TX channel 1 CRC data input mask target register                                              | 0x0300  | R/W    |
| AHB_DMA_TX_CH_ARB_WEIGH_CH1_REG           | TX channel 1 arbitration weight configuration register                                        | 0x0304  | R/W    |
| AHB_DMA_TX_ARB_WEIGH_OPT_DIR_CH1_REG      | TX channel 1 weight arbitration optimization enable register                                 | 0x0308  | R/W    |
| AHB_DMA_OUT_CRC_INIT_DATA_CH2_REG         | TX channel 2 CRC initial value configuration register                                         | 0x030C  | R/W    |
```