
```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| DMA2D_IN_ETM_CONF_CH1_REG                 | Configures the ETM of RX channel 1                                         | 0x0648  | R/W    |
| DMA2D_IN_CONFO_CH2_REG                    | Configures the RX channel 2                                                 | 0x0700  | R/W    |
| DMA2D_IN_POP_CH2_REG                      | Configures the FIFO of RX channel 2                                        | 0x0718  | varies |
| DMA2D_IN_LINK_CONF_CH2_REG                | Configures the receive descriptor operations of RX channel 2               | 0x071C  | varies |
| DMA2D_IN_LINK_ADDR_CH2_REG                | Configures the receive descriptor address of RX channel 2                   | 0x0720  | R/W    |
| DMA2D_IN_ARB_CH2_REG                      | Configures the arbitration of RX channel 2                                  | 0x0740  | R/W    |
| DMA2D_IN_ETM_CONF_CH2_REG                 | Configures the ETM of RX channel 2                                          | 0x0748  | R/W    |
| DMA2D_RST_CONF_REG                        | Configures the reset of AXI                                                 | 0x0A04  | R/W    |
| DMA2D_INTR_MEM_START_ADDR_REG             | The start address of accessible internal memory address space               | 0x0A08  | R/W    |
| DMA2D_INTR_MEM_END_ADDR_REG               | The end address of accessible internal memory address space                 | 0x0A0C  | R/W    |
| DMA2D_EXTR_MEM_START_ADDR_REG             | The start address of accessible external memory address space               | 0x0A10  | R/W    |
| DMA2D_EXTR_MEM_END_ADDR_REG               | The end address of accessible external memory address space                 | 0x0A14  | R/W    |
| DMA2D_OUT_ARB_CONFIG_REG                  | Configures the arbitration in TX direction                                 | 0x0A18  | R/W    |
| DMA2D_IN_ARB_CONFIG_REG                   | Configures the arbitration in RX direction                                 | 0x0A1C  | R/W    |

Interrupt Registers
| Name                                       | Description                                                                 | Address | Access   |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|----------|
| DMA2D_OUT_INT_RAW_CHO_REG                 | Raw interrupt status of TX channel 0                                        | 0x0004  | R/WTC/SS |
| DMA2D_OUT_INT_ENA_CHO_REG                 | Interrupt enable bits of TX channel 0                                       | 0x0008  | R/W      |
| DMA2D_OUT_INT_ST_CHO_REG                  | Masked interrupt status of TX channel 0                                     | 0x000C  | RO       |
| DMA2D_OUT_INT_CLR_CHO_REG                 | Interrupt clear bits of TX channel 0                                         | 0x0010  | WT       |
| DMA2D_OUT_INT_RAW_CH1_REG                 | Raw interrupt status of TX channel 1                                        | 0x0104  | R/WTC/SS |
| DMA2D_OUT_INT_ENA_CH1_REG                 | Interrupt enable bits of TX channel 1                                       | 0x0108  | R/W      |
| DMA2D_OUT_INT_ST_CH1_REG                  | Masked interrupt status of TX channel 1                                     | 0x010C  | RO       |
| DMA2D_OUT_INT_CLR_CH1_REG                 | Interrupt clear bits of TX channel 1                                         | 0x0110  | WT       |
| DMA2D_OUT_INT_RAW_CH2_REG                 | Raw interrupt status of TX channel 2                                        | 0x0204  | R/WTC/SS |
| DMA2D_OUT_INT_ENA_CH2_REG                 | Interrupt enable bits of TX channel 2                                       | 0x0208  | R/W      |
| DMA2D_OUT_INT_ST_CH2_REG                  | Masked interrupt status of TX channel 2                                     | 0x020C  | RO       |
| DMA2D_OUT_INT_CLR_CH2_REG                 | Interrupt clear bits of TX channel 2                                         | 0x0210  | WT       |
| DMA2D_OUT_INT_RAW_CH3_REG                 | Raw interrupt status of TX channel 3                                        | 0x0304  | R/WTC/SS |
| DMA2D_OUT_INT_ENA_CH3_REG                 | Interrupt enable bits of TX channel 3                                       | 0x0308  | R/W      |
```