

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_OUT_EOF_DES_ADDR_CHO_REG           | Transmit descriptor address when EOF occurs on TX channel 0                                      | 0x00E8  | RO     |
| AHB_DMA_OUT_EOF_BFR_DES_ADDR_CHO_REG       | The last transmit descriptor address when EOF occurs on TX channel 0                             | 0x00EC  | RO     |
| AHB_DMA_OUT_DSCR_CHO_REG                   | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 0 | 0x00F0  | RO     |
| AHB_DMA_OUT_DSCR_BFO_CHO_REG               | Address of the current pre-read transmit descriptor on TX channel 0                              | 0x00F4  | RO     |
| AHB_DMA_OUT_DSCR_BF1_CHO_REG               | Address of the previous pre-read transmit descriptor on TX channel 0                             | 0x00F8  | RO     |
| AHB_DMA_IN_DONE_DES_ADDR_CHO_REG           | Address of the completed inlink descriptor on RX channel 0                                       | 0x00B0  | RO     |
| AHB_DMA_OUT_DONE_DES_ADDR_CHO_REG          | Address of the completed outlink descriptor on TX channel 0                                      | 0x0110  | RO     |
| AHB_DMA_INFIFO_STATUS_CH1_REG              | RX channel 1 FIFO status                                                                         | 0x0138  | RO     |
| AHB_DMA_IN_STATE_CH1_REG                   | RX channel 1 status                                                                              | 0x0144  | RO     |
| AHB_DMA_IN_SUC_EOF_DES_ADDR_CH1_REG        | Receive descriptor address when EOF occurs on RX channel 1                                        | 0x0148  | RO     |
| AHB_DMA_IN_DSCR_CH1_REG                    | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 1 | 0x0150  | RO     |
| AHB_DMA_IN_DSCR_BFO_CH1_REG                | Address of the current pre-read receive descriptor on RX channel 1                               | 0x0154  | RO     |
| AHB_DMA_IN_DSCR_BF1_CH1_REG                | Address of the previous pre-read receive descriptor on RX channel 1                              | 0x0158  | RO     |
| AHB_DMA_OUTFIFO_STATUS_CH1_REG             | TX channel 1 FIFO status                                                                         | 0x0198  | RO     |
| AHB_DMA_OUT_STATE_CH1_REG                  | TX channel 1 status                                                                              | 0x01A4  | RO     |
| AHB_DMA_OUT_EOF_DES_ADDR_CH1_REG           | Transmit descriptor address when EOF occurs on TX channel 1                                       | 0x01A8  | RO     |
```