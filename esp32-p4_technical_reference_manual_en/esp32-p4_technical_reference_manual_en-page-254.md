

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| AXI_DMA_OUT_INT_CLR_CH2_REG               | TX channel 2 interrupt clear register                                                            | 0x0214    | WT     |
| Configuration Registers                    |                                              |           |        |
| AXI_DMA_IN_CONFO_CHO_REG                  | Configuration register 0 of RX channel 0                                                        | 0x0010    | R/W    |
| AXI_DMA_IN_CONF1_CHO_REG                  | Configuration register 1 of RX channel 0                                                        | 0x0014    | R/W    |
| AXI_DMA_IN_POP_CHO_REG                    | Pop control register of RX channel 0                                                            | 0x001C    | varies |
| AXI_DMA_IN_LINK1_CHO_REG                  | Linked list descriptor configuration and control register 1 of RX channel 0                     | 0x0020    | varies |
| AXI_DMA_IN_LINK2_CHO_REG                  | Linked list descriptor configuration and control register 2 of RX channel 0                     | 0x0024    | R/W    |
| AXI_DMA_IN_CRC_INIT_DATA_CHO_REG          | RX channel 0 CRC initial value configuration register                                           | 0x0048    | R/W    |
| AXI_DMA_RX_CRC_WIDTH_CHO_REG              | RX channel 0 CRC result width configuration register                                           | 0x004C    | R/W    |
| AXI_DMA_IN_CRC_CLEAR_CHO_REG              | RX channel 0 CRC result clear register                                                          | 0x0050    | R/W    |
| AXI_DMA_IN_CRC_FINAL_RESULT_CHO_REG       | RX channel 0 CRC result register                                                                | 0x0054    | RO     |
| AXI_DMA_RX_CRC_EN_ADDR_CHO_REG            | TX channel 0 CRC intermediate result mask target register                                       | 0x005C    | R/W    |
| AXI_DMA_RX_CRC_DATA_EN_WR_DATA_CHO_REG    | CRC RX channel 0 CRC intermediate result mask register                                         | 0x0060    | R/W    |
| AXI_DMA_RX_CRC_DATA_EN_ADDR_CHO_REG       | RX channel 0 CRC data input mask target register                                                | 0x0064    | R/W    |
| AXI_DMA_IN_CONFO_CH1_REG                  | Configuration register 0 of RX channel 1                                                        | 0x0078    | R/W    |
| AXI_DMA_IN_CONF1_CH1_REG                  | Configuration register 1 of RX channel 1                                                        | 0x007C    | R/W    |
| AXI_DMA_IN_POP_CH1_REG                    | Pop control register of RX channel 1                                                            | 0x0084    | varies |
| AXI_DMA_IN_LINK1_CH1_REG                  | Linked list descriptor configuration and control register 1 of RX channel 1                     | 0x0088    | varies |
| AXI_DMA_IN_LINK2_CH1_REG                  | Linked list descriptor configuration and control register 2 of RX channel 1                     | 0x008C    | R/W    |
| AXI_DMA_IN_CRC_INIT_DATA_CH1_REG          | RX channel 1 CRC initial value configuration register                                           | 0x00B0    | R/W    |
| AXI_DMA_RX_CRC_WIDTH_CH1_REG              | RX channel 1 CRC result width configuration register                                            | 0x00B4    | R/W    |
| AXI_DMA_IN_CRC_CLEAR_CH1_REG              | RX channel 1 CRC result clear register                                                          | 0x00B8    | R/W    |
| AXI_DMA_IN_CRC_FINAL_RESULT_CH1_REG       | RX channel 1 CRC result register                                                                | 0x00BC    | RO     |
| AXI_DMA_RX_CRC_EN_ADDR_CH1_REG            | RX channel 1 CRC intermediate result mask target register                                       | 0x00C4    | R/W    |
| AXI_DMA_RX_CRC_DATA_EN_WR_DATA_CH1_REG    | CRC RX channel 1 CRC intermediate result mask register                                         | 0x00C8    | R/W    |
```