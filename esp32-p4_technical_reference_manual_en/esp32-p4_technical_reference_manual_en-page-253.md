
```markdown
| Name                                       | Description                                                                                      | Address   | Access    |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|-----------|
| Interrupt Registers                        |                                                                                                  |           |           |
| AXI_DMA_IN_INT_RAW_CHO_REG                 | RX channel 0 raw interrupt status register                                                       | 0x0000    | R/WTC/SS  |
| AXI_DMA_IN_INT_ST_CHO_REG                  | RX channel 0 masked interrupt status register                                                  | 0x0004    | RO        |
| AXI_DMA_IN_INT_ENA_CHO_REG                 | RX channel 0 interrupt enable register                                                          | 0x0008    | R/W       |
| AXI_DMA_IN_INT_CLR_CHO_REG                 | RX channel 0 interrupt clear register                                                           | 0x000C    | WT        |
| AXI_DMA_IN_INT_RAW_CH1_REG                 | RX channel 1 raw interrupt status register                                                      | 0x0068    | R/WTC/SS  |
| AXI_DMA_IN_INT_ST_CH1_REG                  | RX channel 1 masked interrupt status register                                                  | 0x006C    | RO        |
| AXI_DMA_IN_INT_ENA_CH1_REG                 | RX channel 1 interrupt enable register                                                          | 0x0070    | R/W       |
| AXI_DMA_IN_INT_CLR_CH1_REG                 | RX channel 1 interrupt clear register                                                           | 0x0074    | WT        |
| AXI_DMA_IN_INT_RAW_CH2_REG                 | RX channel 2 raw interrupt status register                                                      | 0x00D0    | R/WTC/SS  |
| AXI_DMA_IN_INT_ST_CH2_REG                  | RX channel 2 masked interrupt status register                                                  | 0x00D4    | RO        |
| AXI_DMA_IN_INT_ENA_CH2_REG                 | RX channel 2 interrupt enable register                                                          | 0x00D8    | R/W       |
| AXI_DMA_IN_INT_CLR_CH2_REG                 | RX channel 2 interrupt clear register                                                           | 0x00DC    | WT        |
| AXI_DMA_OUT_INT_RAW_CHO_REG                | TX channel 0 raw interrupt status register                                                      | 0x0138    | R/WTC/SS  |
| AXI_DMA_OUT_INT_ST_CHO_REG                 | TX channel 0 masked interrupt status register                                                  | 0x013C    | RO        |
| AXI_DMA_OUT_INT_ENA_CHO_REG                | TX channel 0 interrupt enable register                                                          | 0x0140    | R/W       |
| AXI_DMA_OUT_INT_CLR_CHO_REG                | TX channel 0 interrupt clear register                                                           | 0x0144    | WT        |
| AXI_DMA_OUT_INT_RAW_CH1_REG                | TX channel 1 raw interrupt status register                                                      | 0x01A0    | R/WTC/SS  |
| AXI_DMA_OUT_INT_ST_CH1_REG                 | TX channel 1 masked interrupt status register                                                  | 0x01A4    | RO        |
| AXI_DMA_OUT_INT_ENA_CH1_REG                | TX channel 1 interrupt enable register                                                          | 0x01A8    | R/W       |
| AXI_DMA_OUT_INT_CLR_CH1_REG                | TX channel 1 interrupt clear register                                                           | 0x01AC    | WT        |
| AXI_DMA_OUT_INT_RAW_CH2_REG                | TX channel 2 raw interrupt status register                                                      | 0x0208    | R/WTC/SS  |
| AXI_DMA_OUT_INT_ST_CH2_REG                 | TX channel 2 masked interrupt status register                                                  | 0x020C    | RO        |
| AXI_DMA_OUT_INT_ENA_CH2_REG                | TX channel 2 interrupt enable register                                                          | 0x0210    | R/W       |
```