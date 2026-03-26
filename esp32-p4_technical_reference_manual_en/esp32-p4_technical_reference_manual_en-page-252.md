

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_OUT_DSCR_BF1_CH2_REG              | Address of the previous pre-read transmit descriptor on TX channel 2                             | 0x0278  | RO     |
| AHB_DMA_AHBINF_RESP_ERR_STATUSO_REG       | Address of the transfer for which AHB DMA received an AHB bus error response                    | 0x0408  | RO     |
| AHB_DMA_AHBINF_RESP_ERR_STATUS1_REG       | Transfer type, ID, and channel ID of the transfer for which AHB DMA received an AHB bus error response | 0x040C  | RO     |
| AHB_DMA_IN_DONE_DES_ADDR_CHO_REG          | Address of the completed descriptor for RX channel 0                                             | 0x0410  | RO     |
| AHB_DMA_OUT_DONE_DES_ADDR_CHO_REG         | Address of the completed descriptor for TX channel 0                                             | 0x0414  | RO     |
| AHB_DMA_IN_DONE_DES_ADDR_CH1_REG          | Address of the completed descriptor for RX channel 1                                             | 0x0418  | RO     |
| AHB_DMA_OUT_DONE_DES_ADDR_CH1_REG         | Address of the completed descriptor for TX channel 1                                             | 0x041C  | RO     |
| AHB_DMA_IN_DONE_DES_ADDR_CH2_REG          | Address of the completed descriptor for RX channel 2                                             | 0x0420  | RO     |
| AHB_DMA_OUT_DONE_DES_ADDR_CH2_REG         | Address of the completed descriptor for TX channel 2                                             | 0x0424  | RO     |
| Priority Registers                         |                                                                                                  |         |        |
| AHB_DMA_IN_PRI_CHO_REG                     | Priority register of RX channel 0                                                               | 0x009C  | R/W    |
| AHB_DMA_OUT_PRI_CHO_REG                    | Priority register of TX channel 0                                                               | 0x00FC  | R/W    |
| AHB_DMA_IN_PRI_CH1_REG                     | Priority register of RX channel 1                                                               | 0x015C  | R/W    |
| AHB_DMA_OUT_PRI_CH1_REG                    | Priority register of TX channel 1                                                               | 0x01BC  | R/W    |
| AHB_DMA_IN_PRI_CH2_REG                     | Priority register of RX channel 2                                                               | 0x021C  | R/W    |
| AHB_DMA_OUT_PRI_CH2_REG                    | Priority register of TX channel 2                                                               | 0x027C  | R/W    |
| Peripheral Select Registers                |                                                                                                  |         |        |
| AHB_DMA_IN_PERI_SEL_CHO_REG                | Peripheral selection register of RX channel 0                                                   | 0x00AO  | R/W    |
| AHB_DMA_OUT_PERI_SEL_CHO_REG               | Peripheral selection register of TX channel 0                                                   | 0x0100  | R/W    |
| AHB_DMA_IN_PERI_SEL_CH1_REG                | Peripheral selection register of RX channel 1                                                   | 0x0160  | R/W    |
| AHB_DMA_OUT_PERI_SEL_CH1_REG               | Peripheral selection register of TX channel 1                                                   | 0x01CO  | R/W    |
| AHB_DMA_IN_PERI_SEL_CH2_REG                | Peripheral selection register of RX channel 2                                                   | 0x0220  | R/W    |
| AHB_DMA_OUT_PERI_SEL_CH2_REG               | Peripheral selection register of TX channel 2                                                   | 0x0280  | R/W    |
```