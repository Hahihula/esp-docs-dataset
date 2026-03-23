
```markdown
| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| **Interrupt Registers**                    |                                                                                               |           |        |
| GDMA_IN_INT_RAW_CHO_REG                    | Raw interrupt status of RX channel 0                                                          | 0x0000    | R/WTC/SS |
| GDMA_IN_INT_ST_CHO_REG                     | Masked interrupt status of RX channel 0                                                      | 0x0004    | RO     |
| GDMA_IN_INT_ENA_CHO_REG                    | Interrupt enable bits of RX channel 0                                                        | 0x0008    | R/W    |
| GDMA_IN_INT_CLR_CHO_REG                    | Interrupt clear bits of RX channel 0                                                         | 0x000C    | WT     |
| GDMA_IN_INT_RAW_CH1_REG                    | Raw interrupt status interrupt of TX channel 1                                              | 0x0010    | R/WTC/SS |
| GDMA_IN_INT_ST_CH1_REG                     | Masked interrupt status of TX channel 1                                                      | 0x0014    | RO     |
| GDMA_IN_INT_ENA_CH1_REG                    | Interrupt enable bits of TX channel 1                                                        | 0x0018    | R/W    |
| GDMA_IN_INT_CLR_CH1_REG                    | Interrupt clear bits of TX channel 1                                                         | 0x001C    | WT     |
| GDMA_IN_INT_RAW_CH2_REG                    | Raw interrupt status of RX channel 2                                                         | 0x0020    | R/WTC/SS |
| GDMA_IN_INT_ST_CH2_REG                     | Masked interrupt status of RX channel 2                                                      | 0x0024    | RO     |
| GDMA_IN_INT_ENA_CH2_REG                    | Interrupt enable bits of RX channel 2                                                        | 0x0028    | R/W    |
| GDMA_IN_INT_CLR_CH2_REG                    | Interrupt clear bits of RX channel 2                                                         | 0x002C    | WT     |
| GDMA_OUT_INT_RAW_CHO_REG                   | Raw interrupt status of TX channel 0                                                         | 0x0030    | R/WTC/SS |
| GDMA_OUT_INT_ST_CHO_REG                    | Masked interrupt status of TX channel 0                                                      | 0x0034    | RO     |
| GDMA_OUT_INT_ENA_CHO_REG                   | Interrupt enable bits of TX channel 0                                                        | 0x0038    | R/W    |
| GDMA_OUT_INT_CLR_CHO_REG                   | Interrupt clear bits of TX channel 0                                                         | 0x003C    | WT     |
| GDMA_OUT_INT_RAW_CH1_REG                   | Raw interrupt status of TX channel 1                                                        | 0x0040    | R/WTC/SS |
| GDMA_OUT_INT_ST_CH1_REG                    | Masked interrupt status of TX channel 1                                                      | 0x0044    | RO     |
| GDMA_OUT_INT_ENA_CH1_REG                   | Interrupt enable bits of TX channel 1                                                        | 0x0048    | R/W    |
| GDMA_OUT_INT_CLR_CH1_REG                   | Interrupt clear bits of TX channel 1                                                         | 0x004C    | WT     |
| GDMA_OUT_INT_RAW_CH2_REG                   | Raw interrupt status of TX channel 2                                                         | 0x0050    | R/WTC/SS |
| GDMA_OUT_INT_ST_CH2_REG                    | Masked interrupt status of TX channel 2                                                      | 0x0054    | RO     |
| GDMA_OUT_INT_ENA_CH2_REG                   | Interrupt enable bits of TX channel 2                                                        | 0x0058    | R/W    |
| GDMA_OUT_INT_CLR_CH2_REG                   | Interrupt clear bits of TX channel 2                                                         | 0x005C    | WT     |
| **Debug Registers**                        |                                                                                               |           |        |
| GDMA_AHB_TEST_REG                           | Reserved                                                                                    | 0x0060    | R/W    |
| **Configuration Registers**                |                                                                                               |           |        |
| GDMA_MISC_CONF_REG                          | Miscellaneous register                                                                      | 0x0064    | R/W    |
| GDMA_IN_CONFO_CHO_REG                       | Configuration register 0 of RX channel 0                                                    | 0x0070    | R/W    |
| GDMA_IN_CONF1_CHO_REG                        | Configuration register 1 of RX channel 0                                                    | 0x0074    | R/W    |
| GDMA_IN_POP_CHO_REG                          | Pop control register of RX channel 0                                                        | 0x007C    | varies |
```