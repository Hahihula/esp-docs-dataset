

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AXI_DMA_IN_DSCR_CH1_REG                   | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 1 | 0x009C  | RO     |
| AXI_DMA_IN_DSCR_BFO_CH1_REG               | Address of the current pre-read receive descriptor on RX channel 1                               | 0x00A0  | RO     |
| AXI_DMA_IN_DSCR_BF1_CH1_REG               | Address of the previous pre-read receive descriptor on RX channel 1                              | 0x00A4  | RO     |
| AXI_DMA_INFIFO_STATUS_CH2_REG             | RX channel 2 FIFO status register                                                               | 0x00E8  | RO     |
| AXI_DMA_IN_STATE_CH2_REG                  | RX channel 2 status register                                                                    | 0x00F8  | RO     |
| AXI_DMA_IN_SUC_EOF_DES_ADDR_CH2_REG       | Receive descriptor address when EOF occurs on RX channel 2                                       | 0x00FC  | RO     |
| AXI_DMA_IN_ERR_EOF_DES_ADDR_CH2_REG       | Receive descriptor address when errors occur on RX channel 2                                     | 0x0100  | RO     |
| AXI_DMA_IN_DSCR_CH2_REG                   | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 2 | 0x0104  | RO     |
| AXI_DMA_IN_DSCR_BFO_CH2_REG               | Address of the current pre-read receive descriptor on RX channel 2                               | 0x0108  | RO     |
| AXI_DMA_IN_DSCR_BF1_CH2_REG               | Address of the previous pre-read receive descriptor on RX channel 2                              | 0x010C  | RO     |
| AXI_DMA_OUTFIFO_STATUS_CHO_REG            | TX channel 0 FIFO status                                                                        | 0x0150  | RO     |
| AXI_DMA_OUT_STATE_CHO_REG                 | TX channel 0 status                                                                             | 0x0160  | RO     |
| AXI_DMA_OUT_EOF_DES_ADDR_CHO_REG          | Transmit descriptor address when EOF occurs on TX channel 0                                      | 0x0164  | RO     |
| AXI_DMA_OUT_EOF_BFR_DES_ADDR_CHO_REG      | The last transmit descriptor address when EOF occurs on TX channel 0                            | 0x0168  | RO     |
| AXI_DMA_OUT_DSCR_CHO_REG                  | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 0 | 0x016C  | RO     |
| AXI_DMA_OUT_DSCR_BFO_CHO_REG              | Address of the current pre-read transmit descriptor on TX channel 0                             | 0x0170  | RO     |
| AXI_DMA_OUT_DSCR_BF1_CHO_REG              | Address of the previous pre-read transmit descriptor on TX channel 0                            | 0x0174  | RO     |
| AXI_DMA_OUTFIFO_STATUS_CH1_REG            | TX channel 0 FIFO status                                                                        | 0x01B8  | RO     |
| AXI_DMA_OUT_STATE_CH1_REG                 | TX channel 1 status                                                                             | 0x01C8  | RO     |
```