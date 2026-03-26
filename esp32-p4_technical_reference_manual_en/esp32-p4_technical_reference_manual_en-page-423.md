
```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| DMA2D_OUT_INT_ST_CH3_REG                  | Masked interrupt status of TX channel 3                                    | 0x030C    | RO     |
| DMA2D_OUT_INT_CLR_CH3_REG                 | Interrupt clear bits of TX channel 3                                        | 0x0310    | WT     |
| DMA2D_IN_INT_RAW_CHO_REG                  | Raw interrupt status of RX channel 0                                        | 0x0504    | R/WTC/SS|
| DMA2D_IN_INT_ENA_CHO_REG                  | Interrupt enable bits of RX channel 0                                       | 0x0508    | R/W    |
| DMA2D_IN_INT_ST_CHO_REG                   | Masked interrupt status of RX channel 0                                      | 0x050C    | RO     |
| DMA2D_IN_INT_CLR_CHO_REG                  | Interrupt clear bits of RX channel 0                                         | 0x0510    | WT     |
| DMA2D_IN_INT_RAW_CH1_REG                  | Raw interrupt status of RX channel 1                                         | 0x0604    | R/WTC/SS|
| DMA2D_IN_INT_ENA_CH1_REG                  | Interrupt enable bits of RX channel 1                                        | 0x0608    | R/W    |
| DMA2D_IN_INT_ST_CH1_REG                   | Masked interrupt status of RX channel 1                                      | 0x060C    | RO     |
| DMA2D_IN_INT_CLR_CH1_REG                  | Interrupt clear bits of RX channel 1                                         | 0x0610    | WT     |
| DMA2D_IN_INT_RAW_CH2_REG                  | Raw interrupt status of RX channel 2                                         | 0x0704    | R/WTC/SS|
| DMA2D_IN_INT_ENA_CH2_REG                  | Interrupt enable bits of RX channel 2                                        | 0x0708    | R/W    |
| DMA2D_IN_INT_ST_CH2_REG                   | Masked interrupt status of RX channel 2                                      | 0x070C    | RO     |
| DMA2D_IN_INT_CLR_CH2_REG                  | Interrupt clear bits of RX channel 2                                         | 0x0710    | WT     |

Status Registers
-----------------
DMA2D_OUTFIFO_STATUS_CHO_REG               | Represents the status of the FIFO of TX channel 0                            | 0x0014    | RO     |
DMA2D_OUT_STATE_CHO_REG                    | Represents the working status of the transmit descriptor of TX channel 0      | 0x0024    | RO     |
DMA2D_OUT_EOF_DES_ADDR_CHO_REG             | Represents the transmit descriptor address when EOF occurs on TX channel 0    | 0x0028    | RO     |
DMA2D_OUT_DSCR_CHO_REG                     | Represents the address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 0 | 0x002C    | RO     |
DMA2D_OUT_DSCR_BFO_CHO_REG                 | Represents the address of the current pre-read transmit descriptor on TX channel 0 | 0x0030    | RO     |
DMA2D_OUT_DSCR_BF1_CHO_REG                 | Represents the address of the previous pre-read transmit descriptor on TX channel 0 | 0x0034    | RO     |
DMA2D_OUTFIFO_STATUS_CH1_REG               | Represents the status of the FIFO of TX channel 1                            | 0x0114    | RO     |
DMA2D_OUT_STATE_CH1_REG                    | Represents the working status of the transmit descriptor of TX channel 1      | 0x0124    | RO     |
DMA2D_OUT_EOF_DES_ADDR_CH1_REG             | Represents the transmit descriptor address when EOF occurs on TX channel 1    | 0x0128    | RO     |
```