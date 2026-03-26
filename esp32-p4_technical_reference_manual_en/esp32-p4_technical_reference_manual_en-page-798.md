

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| CORE1_H264_DMA2D_OUT_CH4_INT_MAP_REG      | H264_DMA2D_OUT_CH4_INTR mapping register                                                        | 0x01DC  | R/W    |
| CORE1_H264_DMA2D_IN_CHO_INT_MAP_REG       | H264_DMA2D_IN_CHO_INTR mapping register                                                         | 0x01EO  | R/W    |
| CORE1_H264_DMA2D_IN_CH1_INT_MAP_REG       | H264_DMA2D_IN_CH1_INTR mapping register                                                        | 0x01E4  | R/W    |
| CORE1_H264_DMA2D_IN_CH2_INT_MAP_REG       | H264_DMA2D_IN_CH2_INTR mapping register                                                        | 0x01E8  | R/W    |
| CORE1_H264_DMA2D_IN_CH3_INT_MAP_REG       | H264_DMA2D_IN_CH3_INTR mapping register                                                        | 0x01EC  | R/W    |
| CORE1_H264_DMA2D_IN_CH4_INT_MAP_REG       | H264_DMA2D_IN_CH4_INTR mapping register                                                        | 0x01FO  | R/W    |
| CORE1_H264_DMA2D_IN_CH5_INT_MAP_REG       | H264_DMA2D_IN_CH5_INTR mapping register                                                        | 0x01F4  | R/W    |
| CORE1_H264_REG_INT_MAP_REG                 | H264_REG_INTR mapping register                                                                 | 0x01F8  | R/W    |
| CORE1_ASSIST_DEBUG_INT_MAP_REG             | ASSIST_DEBUG_INTR mapping register                                                              | 0x01FC  | R/W    |
| CORE1_INTR_STATUS_REG_0_REG                | Status register for interrupt sources 0 ~ 31                                                   | 0x0200  | RO     |
| CORE1_INTR_STATUS_REG_1_REG                | Status register for interrupt sources 32 ~ 63                                                 | 0x0204  | RO     |
| CORE1_INTR_STATUS_REG_2_REG                | Status register for interrupt sources 64 ~ 95                                                 | 0x0208  | RO     |
| CORE1_INTR_STATUS_REG_3_REG                | Status register for interrupt sources 96 ~ 127                                                | 0x020C  | RO     |
| CORE1_CLOCK_GATE_REG                       | Clock gating register                                                                           | 0x0210  | R/W    |
| CORE1_DMA2D_IN_CH2_INT_MAP_REG             | DMA2D_IN_CH2_INTR mapping register                                                             | 0x214   | R/W    |
| CORE1_DMA2D_OUT_CH3_INT_MAP_REG            | DMA2D_OUT_CH3_INTR mapping register                                                            | 0x218   | R/W    |
| CORE1_AXI_PERF_MON_INT_MAP_REG             | AXI_PERF_MON_INTR mapping register                                                             | 0x21C   | R/W    |
| CORE1_INTR_STATUS_REG_4_REG                | Status register for interrupt sources 128 ~ 130                                               | 0x0220  | RO     |
| CORE1_INTR_SIG_IDX_ASSERT_IN_SEC_REG       | CORE1 interrupt delegation configuration register                                             | 0x0228  | R/W    |
| CORE1_INTR_SEC_STATUS_REG                  | CORE1 interrupt delegation status register                                                     | 0x022C  | RO     |
| CORE1_INTR_SRC_PASS_IN_SEC_STATUS_0_REG    | Interrupt delegation status register for interrupt sources 0 ~ 31                               | 0x0230  | RO     |
| CORE1_INTR_SRC_PASS_IN_SEC_STATUS_1_REG    | Interrupt delegation status register for interrupt sources 32 ~ 63                              | 0x0234  | RO     |
| CORE1_INTR_SRC_PASS_IN_SEC_STATUS_2_REG    | Interrupt delegation status register for interrupt sources 64 ~ 95                              | 0x0238  | RO     |
```