

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| AHB_DMA_OUT_EOF_DES_ADDR_CH1_REG           | Transmit descriptor address when EOF occurs on TX channel 1                                      | 0x01A8    | RO     |
| AHB_DMA_OUT_EOF_BFR_DES_ADDR_CH1_REG       | The last transmit descriptor address when EOF occurs on TX channel 1                            | 0x01AC    | RO     |
| AHB_DMA_OUT_DSCR_CH1_REG                   | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 1 | 0x01BO    | RO     |
| AHB_DMA_OUT_DSCR_BFO_CH1_REG               | Address of the current pre-read transmit descriptor on TX channel 1                             | 0x01B4    | RO     |
| AHB_DMA_OUT_DSCR_BF1_CH1_REG               | Address of the previous pre-read transmit descriptor on TX channel 1                           | 0x01B8    | RO     |
| AHB_DMA_INFIFO_STATUS_CH2_REG              | RX channel 2 FIFO status                                                                        | 0x01F8    | RO     |
| AHB_DMA_IN_STATE_CH2_REG                   | RX channel 2 status                                                                             | 0x0204    | RO     |
| AHB_DMA_IN_SUC_EOF_DES_ADDR_CH2_REG        | Receive descriptor address when EOF occurs on RX channel 2                                       | 0x0208    | RO     |
| AHB_DMA_IN_ERR_EOF_DES_ADDR_CH2_REG        | Receive descriptor address when errors occur on RX channel 2                                     | 0x020C    | RO     |
| AHB_DMA_IN_DSCR_CH2_REG                    | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 2 | 0x0210    | RO     |
| AHB_DMA_IN_DSCR_BFO_CH2_REG                | Address of the current pre-read receive descriptor on RX channel 2                              | 0x0214    | RO     |
| AHB_DMA_IN_DSCR_BF1_CH2_REG                | Address of the previous pre-read receive descriptor on RX channel 2                             | 0x0218    | RO     |
| AHB_DMA_OUTFIFO_STATUS_CH2_REG             | TX channel 2 FIFO status                                                                        | 0x0258    | RO     |
| AHB_DMA_OUT_STATE_CH2_REG                  | TX channel 2 status                                                                             | 0x0264    | RO     |
| AHB_DMA_OUT_EOF_DES_ADDR_CH2_REG           | Transmit descriptor address when EOF occurs on TX channel 2                                      | 0x0268    | RO     |
| AHB_DMA_OUT_EOF_BFR_DES_ADDR_CH2_REG       | The last transmit descriptor address when EOF occurs on TX channel 2                            | 0x026C    | RO     |
| AHB_DMA_OUT_DSCR_CH2_REG                   | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 2 | 0x0270    | RO     |
| AHB_DMA_OUT_DSCR_BFO_CH2_REG               | Address of the current pre-read transmit descriptor on TX channel 2                             | 0x0274    | RO     |
```