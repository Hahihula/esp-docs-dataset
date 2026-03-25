

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_IN_LINK_ADDR_CH1_REG              | Linked list descriptor configuration register of RX channel 1                                    | 0x03BO  | R/W    |
| AHB_DMA_OUT_LINK_ADDR_CHO_REG             | Linked list descriptor configuration register of TX channel 0                                   | 0x03B8  | R/W    |
| AHB_DMA_OUT_LINK_ADDR_CH1_REG             | Linked list descriptor configuration register of TX channel 1                                   | 0x03BC  | R/W    |
| AHB_DMA_INTR_MEM_START_ADDR_REG           | Accessible address space start address configuration register                                  | 0x03C4  | R/W    |
| AHB_DMA_INTR_MEM_END_ADDR_REG             | Accessible address space end address configuration register                                    | 0x03C8  | R/W    |
| AHB_DMA_ARB_TIMEOUT_TX_REG                | TX arbitration timeout configuration register                                                  | 0x03CC  | R/W    |
| AHB_DMA_ARB_TIMEOUT_RX_REG                | RX arbitration timeout configuration register                                                  | 0x03D0  | R/W    |
| AHB_DMA_WEIGHT_EN_TX_REG                  | TX weight arbitration enable register                                                          | 0x03D4  | R/W    |
| AHB_DMA_WEIGHT_EN_RX_REG                  | RX weight arbitration enable register                                                          | 0x03D8  | R/W    |
| Version Registers                         |                                                                                                  |         |        |
| AHB_DMA_DATE_REG                          | Version control register                                                                       | 0x0068  | R/W    |
| Status Registers                          |                                                                                                  |         |        |
| AHB_DMA_INFIFO_STATUS_CHO_REG             | RX channel 0 FIFO status                                                                        | 0x0078  | RO     |
| AHB_DMA_IN_STATE_CHO_REG                  | RX channel 0 status                                                                             | 0x0084  | RO     |
| AHB_DMA_IN_SUC_EOF_DES_ADDR_CHO_REG       | Receive descriptor address when EOF occurs on RX channel 0                                       | 0x0088  | RO     |
| AHB_DMA_IN_DSCR_CHO_REG                   | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 0 | 0x0090  | RO     |
| AHB_DMA_IN_DSCR_BFO_CHO_REG               | Address of the current pre-read receive descriptor on RX channel 0                              | 0x0094  | RO     |
| AHB_DMA_IN_DSCR_BF1_CHO_REG               | Address of the previous pre-read receive descriptor on RX channel 0                             | 0x0098  | RO     |
| AHB_DMA_OUTFIFO_STATUS_CHO_REG            | TX channel 0 FIFO status                                                                        | 0x00D8  | RO     |
| AHB_DMA_OUT_STATE_CHO_REG                 | TX channel 0 status                                                                             | 0x00E4  | RO     |
```