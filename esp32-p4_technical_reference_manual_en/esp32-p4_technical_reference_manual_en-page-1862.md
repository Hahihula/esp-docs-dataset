

```markdown
| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| H264_DMA_IN_LINK_ADDR_CH4_REG             | RX CH4 in_link dscr addr register                                                            | 0x0920    | R/W    |
| H264_DMA_IN_ARB_CH4_REG                   | RX CH4 arb register                                                                           | 0x0940    | R/W    |
| H264_DMA_IN_CONF0_CH5_REG                 | RX CH5 config0 register                                                                       | 0x0A00    | R/W    |
| H264_DMA_IN_CONF1_CH5_REG                 | RX CH5 config1 register                                                                       | 0x0A04    | R/W    |
| H264_DMA_IN_CONF2_CH5_REG                 | RX CH5 config2 register                                                                       | 0x0A08    | R/W    |
| H264_DMA_IN_CONF3_CH5_REG                 | RX CH5 config3 register                                                                       | 0x0A0C    | R/W    |
| H264_DMA_IN_POP_CH5_REG                   | RX CH5 INFIFO pop register                                                                    | 0x0A24    | varies |
| H264_DMA_IN_ARB_CH5_REG                   | RX CH5 arb register                                                                           | 0x0A40    | R/W    |
| **Other Configuration Registers**         |                                                                                               |           |        |
| H264_DMA_RST_CONF_REG                     | AXI reset config register                                                                     | 0x0B08    | R/W    |
| H264_DMA_INTER_MEM_START_ADDR0_REG       | Start address of internal memory range0 register                                            | 0x0B0C    | R/W    |
| H264_DMA_INTER_MEM_END_ADDR0_REG          | end address of internal memory range0 register                                               | 0x0B10    | R/W    |
| H264_DMA_INTER_MEM_START_ADDR1_REG        | Start address of internal memory range1 register                                            | 0x0B14    | R/W    |
| H264_DMA_INTER_MEM_END_ADDR1_REG          | end address of internal memory range1 register                                               | 0x0B18    | R/W    |
| H264_DMA_EXTER_MEM_START_ADDR0_REG        | Start address of external memory range0 register                                             | 0x0B20    | R/W    |
| H264_DMA_EXTER_MEM_END_ADDR0_REG          | end address of external memory range0 register                                               | 0x0B24    | R/W    |
| H264_DMA_EXTER_MEM_START_ADDR1_REG        | Start address of external memory range1 register                                             | 0x0B28    | R/W    |
| H264_DMA_EXTER_MEM_END_ADDR1_REG          | end address of external memory range1 register                                               | 0x0B2C    | R/W    |
| H264_DMA_OUT_ARB_CONFIG_REG               | reserved                                                                                      | 0x0B30    | R/W    |
| H264_DMA_IN_ARB_CONFIG_REG                | reserved                                                                                      | 0x0B34    | R/W    |
| H264_DMA_COUNTER_RST_REG                  | counter reset register                                                                        | 0x0B50    | R/W    |

**Interrupt Registers**

| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| TX Interrupt Registers                     |                                                                                               |           |        |
| H264_DMA_OUT_INT_RAW_CHO_REG              | TX CHO interrupt raw register                                                                | 0x0004    | R/WTC/SS|
| H264_DMA_OUT_INT_ENA_CHO_REG              | TX CHO interrupt ena register                                                                | 0x0008    | R/W    |
| H264_DMA_OUT_INT_ST_CHO_REG               | TX CHO interrupt st register                                                                  | 0x000C    | RO     |
| H264_DMA_OUT_INT_CLR_CHO_REG              | TX CHO interrupt clr register                                                                 | 0x0010    | WT     |
| H264_DMA_OUT_INT_RAW_CH1_REG              | TX CH1 interrupt raw register                                                                | 0x0104    | R/WTC/SS|
| H264_DMA_OUT_INT_ENA_CH1_REG              | TX CH1 interrupt ena register                                                                | 0x0108    | R/W    |
| H264_DMA_OUT_INT_ST_CH1_REG               | TX CH1 interrupt st register                                                                  | 0x010C    | RO     |
| H264_DMA_OUT_INT_CLR_CH1_REG              | TX CH1 interrupt clr register                                                                 | 0x0110    | WT     |
| H264_DMA_OUT_INT_RAW_CH2_REG              | TX CH2 interrupt raw register                                                                | 0x0204    | R/WTC/SS|
| H264_DMA_OUT_INT_ENA_CH2_REG              | TX CH2 interrupt ena register                                                                | 0x0208    | R/W    |
| H264_DMA_OUT_INT_ST_CH2_REG               | TX CH2 interrupt st register                                                                  | 0x020C    | RO     |
| H264_DMA_OUT_INT_CLR_CH2_REG              | TX CH2 interrupt clr register                                                                 | 0x0210    | WT     |
```