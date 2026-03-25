

```markdown
| Name                                       | Description                                                                                   | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_OUT_CONF0_CHO_REG                 | Configuration register 0 of TX channel 0                                                     | 0x00D0  | R/W    |
| AHB_DMA_OUT_CONF1_CHO_REG                 | Configuration register 1 of TX channel 0                                                     | 0x00D4  | R/W    |
| AHB_DMA_OUT_PUSH_CHO_REG                  | Push control register of TX channel 0                                                        | 0x00DC  | varies |
| AHB_DMA_OUT_LINK_CHO_REG                  | Linked list descriptor configuration and control register of TX channel 0                    | 0x00E0  | varies |
| AHB_DMA_IN_CONF0_CH1_REG                  | Configuration register 0 of RX channel 1                                                    | 0x0130  | R/W    |
| AHB_DMA_IN_CONF1_CH1_REG                  | Configuration register 1 of RX channel 1                                                    | 0x0134  | R/W    |
| AHB_DMA_IN_POP_CH1_REG                    | Pop control register of RX channel 1                                                         | 0x013C  | varies |
| AHB_DMA_IN_LINK_CH1_REG                   | Linked list descriptor configuration and control register of RX channel 1                    | 0x0140  | varies |
| AHB_DMA_OUT_CONF0_CH1_REG                 | Configuration register 0 of TX channel 1                                                    | 0x0190  | R/W    |
| AHB_DMA_OUT_CONF1_CH1_REG                 | Configuration register 1 of TX channel 1                                                    | 0x0194  | R/W    |
| AHB_DMA_OUT_PUSH_CH1_REG                  | Push control register of TX channel 1                                                        | 0x019C  | varies |
| AHB_DMA_OUT_LINK_CH1_REG                  | Linked list descriptor configuration and control register of TX channel 1                    | 0x01A0  | varies |
| AHB_DMA_TX_CH_ARB_WEIGH_CHO_REG           | TX channel 0 arbitration weight configuration register                                      | 0x02DC  | R/W    |
| AHB_DMA_TX_CH_ARB_WEIGH_OPT_DIR_CHO_REG   | TX channel 0 weight arbitration optimization enable register                                | 0x02E0  | R/W    |
| AHB_DMA_TX_CH_ARB_WEIGH_CH1_REG           | TX channel 1 arbitration weight configuration register                                      | 0x0304  | R/W    |
| AHB_DMA_TX_CH_ARB_WEIGH_OPT_DIR_CH1_REG   | TX channel 1 weight arbitration optimization enable register                                | 0x0308  | R/W    |
| AHB_DMA_RX_CH_ARB_WEIGH_CHO_REG           | RX channel 0 arbitration weight configuration register                                      | 0x0354  | R/W    |
| AHB_DMA_RX_CH_ARB_WEIGH_OPT_DIR_CHO_REG   | RX channel 0 weight arbitration optimization enable register                                | 0x0358  | R/W    |
| AHB_DMA_RX_CH_ARB_WEIGH_CH1_REG           | RX channel 1 arbitration weight configuration register                                      | 0x037C  | R/W    |
| AHB_DMA_RX_CH_ARB_WEIGH_OPT_DIR_CH1_REG   | RX channel 1 weight arbitration optimization enable register                                | 0x0380  | R/W    |
| AHB_DMA_IN_LINK_ADDR_CHO_REG              | Linked list descriptor configuration register of RX channel 0                               | 0x03AC  | R/W    |
```