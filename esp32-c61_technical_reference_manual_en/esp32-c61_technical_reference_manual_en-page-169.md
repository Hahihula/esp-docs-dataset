

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_OUT_EOF_BFR_DESC_ADDR_CH1_REG      | The last transmit descriptor address when EOF occurs on TX channel 1                               | 0x01AC  | RO     |
| AHB_DMA_OUT_DSCR_CH1_REG                   | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 1 | 0x01BO  | RO     |
| AHB_DMA_OUT_DSCR_BFO_CH1_REG               | Address of the current pre-read transmit descriptor on TX channel 1                               | 0x01B4  | RO     |
| AHB_DMA_OUT_DSCR_BF1_CH1_REG               | Address of the previous pre-read transmit descriptor on TX channel 1                             | 0x01B8  | RO     |
| AHB_DMA_IN_DONE_DESC_ADDR_CH1_REG          | Address of the completed inlink descriptor on RX channel 1                                       | 0x0170  | RO     |
| AHB_DMA_OUT_DONE_DESC_ADDR_CH1_REG         | Address of the completed outlink descriptor on TX channel 1                                      | 0x01DO  | RO     |

**Priority Registers**

| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_IN_PRI_CHO_REG                     | Priority register of RX channel 0                                                                | 0x009C  | R/W    |
| AHB_DMA_OUT_PRI_CHO_REG                    | Priority register of TX channel 0                                                                | 0x00FC  | R/W    |
| AHB_DMA_IN_PRI_CH1_REG                     | Priority register of RX channel 1                                                                | 0x015C  | R/W    |
| AHB_DMA_OUT_PRI_CH1_REG                    | Priority register of TX channel 1                                                                | 0x01BC  | R/W    |

**Peripheral Selection Registers**

| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_IN_PERI_SEL_CHO_REG                | Peripheral selection register of RX channel 0                                                   | 0x00A0  | R/W    |
| AHB_DMA_OUT_PERI_SEL_CH0_REG               | Peripheral selection register of TX channel 0                                                   | 0x0100  | R/W    |
| AHB_DMA_IN_PERI_SEL_CH1_REG                | Peripheral selection register of RX channel 1                                                   | 0x0160  | R/W    |
| AHB_DMA_OUT_PERI_SEL_CH1_REG               | Peripheral selection register of TX channel 1                                                   | 0x01CO  | R/W    |
```