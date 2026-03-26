

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| AHB_DMA_OUT_INT_ST_CH2_REG                | TX channel 2 masked interrupt status register                               | 0x0054    | RO     |
| AHB_DMA_OUT_INT_ENA_CH2_REG               | TX channel 2 interrupt enable register                                     | 0x0058    | R/W    |
| AHB_DMA_OUT_INT_CLR_CH2_REG               | TX channel 2 interrupt clear register                                      | 0x005C    | WT     |
| Debug Registers                            |                                                                             |           |        |
| AHB_DMA_AHB_TEST_REG                      | Reserved                                                                   | 0x0060    | R/W    |
| Configuration Registers                   |                                                                             |           |        |
| AHB_DMA_MISC_CONF_REG                     | Miscellaneous register                                                     | 0x0064    | R/W    |
| AHB_DMA_IN_CONFO_CHO_REG                  | Configuration register 0 of RX channel 0                                   | 0x0070    | R/W    |
| AHB_DMA_IN_CONF1_CHO_REG                  | Configuration register 1 of Rx channel 0                                   | 0x0074    | R/W    |
| AHB_DMA_IN_POP_CHO_REG                    | Pop control register of RX channel 0                                       | 0x007C    | varies |
| AHB_DMA_IN_LINK_CHO_REG                   | Linked list descriptor configuration and control register of RX channel 0   | 0x0080    | varies |
| AHB_DMA_OUT_CONFO_CHO_REG                 | Configuration register 0 of TX channel 0                                   | 0x00D0    | R/W    |
| AHB_DMA_OUT_CONF1_CHO_REG                 | Configuration register 1 of TX channel 0                                   | 0x00D4    | R/W    |
| AHB_DMA_OUT_PUSH_CHO_REG                  | Push control register of TX channel 0                                      | 0x00DC    | varies |
| AHB_DMA_OUT_LINK_CHO_REG                  | Linked list descriptor configuration and control register of TX channel 0   | 0x00E0    | varies |
| AHB_DMA_IN_CONFO_CH1_REG                  | Configuration register 0 of RX channel 1                                   | 0x0130    | R/W    |
| AHB_DMA_IN_CONF1_CH1_REG                  | Configuration register 1 of RX channel 1                                   | 0x0134    | R/W    |
| AHB_DMA_IN_POP_CH1_REG                    | Pop control register of RX channel 1                                       | 0x013C    | varies |
| AHB_DMA_IN_LINK_CH1_REG                   | Linked list descriptor configuration and control register of RX channel 1   | 0x0140    | varies |
| AHB_DMA_OUT_CONFO_CH1_REG                 | Configuration register 0 of TX channel 1                                   | 0x0190    | R/W    |
| AHB_DMA_OUT_CONF1_CH1_REG                 | Configuration register 1 of TX channel 1                                   | 0x0194    | R/W    |
| AHB_DMA_OUT_PUSH_CH1_REG                  | Push control register of TX channel 1                                      | 0x019C    | varies |
| AHB_DMA_OUT_LINK_CH1_REG                  | Linked list descriptor configuration and control register of TX channel 1   | 0x01A0    | varies |
| AHB_DMA_IN_CONFO_CH2_REG                  | Configuration register 0 of RX channel 2                                   | 0x01F0    | R/W    |
| AHB_DMA_IN_CONF1_CH2_REG                  | Configuration register 1 of RX channel 2                                   | 0x01F4    | R/W    |
```