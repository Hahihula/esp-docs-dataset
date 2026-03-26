

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| AXI_DMA_OUT_EOF_DES_ADDR_CH1_REG           | Transmit descriptor address when EOF occurs on TX channel 1                                      | 0x01CC    | RO     |
| AXI_DMA_OUT_EOF_BFR_DES_ADDR_CH1_REG       | The last transmit descriptor address when EOF occurs on TX channel 1                            | 0x01DO    | RO     |
| AXI_DMA_OUT_DSCR_CH1_REG                   | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 1 | 0x01D4    | RO     |
| AXI_DMA_OUT_DSCR_BFO_CH1_REG               | Address of the current pre-read transmit descriptor on TX channel 1                             | 0x01D8    | RO     |
| AXI_DMA_OUT_DSCR_BF1_CH1_REG               | Address of the previous pre-read transmit descriptor on TX channel 1                           | 0x01DC    | RO     |
| AXI_DMA_OUTFIFO_STATUS_CH2_REG             | TX channel 2 FIFO status                                                                        | 0x0220    | RO     |
| AXI_DMA_OUT_STATE_CH2_REG                  | TX channel 2 status                                                                             | 0x0230    | RO     |
| AXI_DMA_OUT_EOF_DES_ADDR_CH2_REG           | Transmit descriptor address when EOF occurs on TX channel 2                                      | 0x0234    | RO     |
| AXI_DMA_OUT_EOF_BFR_DES_ADDR_CH2_REG       | The last transmit descriptor address when EOF occurs on TX channel 2                            | 0x0238    | RO     |
| AXI_DMA_OUT_DSCR_CH2_REG                   | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 2 | 0x023C    | RO     |
| AXI_DMA_OUT_DSCR_BFO_CH2_REG               | Address of the current pre-read transmit descriptor on TX channel 2                             | 0x0240    | RO     |
| AXI_DMA_OUT_DSCR_BF1_CH2_REG               | Address of the previous pre-read transmit descriptor on TX channel 2                           | 0x0244    | RO     |
| AXI_DMA_IN_RESET_AVAIL_CHO_REG             | RX channel 0 reset status register                                                             | 0x028C    | RO     |
| AXI_DMA_IN_RESET_AVAIL_CH1_REG             | RX channel 1 reset status register                                                             | 0x0290    | RO     |
| AXI_DMA_IN_RESET_AVAIL_CH2_REG             | RX channel 2 reset status register                                                             | 0x0294    | RO     |
| AXI_DMA_OUT_RESET_AVAIL_CHO_REG            | TX channel 0 reset status register                                                             | 0x0298    | RO     |
| AXI_DMA_OUT_RESET_AVAIL_CH1_REG            | TX channel 1 reset status register                                                             | 0x029C    | RO     |
| AXI_DMA_OUT_RESET_AVAIL_CH2_REG            | TX channel 2 reset status register                                                             | 0x02A0    | RO     |
| Priority Registers                          |                                                                                                  |           |        |
| AXI_DMA_IN_PRI_CHO_REG                     | Priority register of RX channel 0                                                              | 0x0040    | R/W    |
| AXI_DMA_IN_PRI_CH1_REG                     | Priority register of RX channel 1                                                              | 0x00A8    | R/W    |
```