

```markdown
| No. | Chapter                  | Interrupt Source   | Interrupt Source Mapping Register                                                                                   | Bit | Interrupt Status Register Name                     |
|-----|--------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------|-----|----------------------------------------------------|
| 64  | Reset and Clock          | SLC0_INTR          | INTMTX_COREO_SLC0_INTR_MAP_REG                                                                                      | 0   |                                                    |
| 65  | Reset and Clock          | SLC1_INTR          | INTMTX_COREO_SLC1_INTR_MAP_REG                                                                                      | 1   |                                                    |
| 66  | GDMA Controller (GDMA)   | GDMA_IN_CHO_INTR   | INTMTX_COREO_DMA_IN_CHO_INTR_MAP_REG                                                                                | 2   |                                                    |
| 67  | GDMA Controller (GDMA)   | GDMA_IN_CH1_INTR   | INTMTX_COREO_DMA_IN_CH1_INTR_MAP_REG                                                                                | 3   |                                                    |
| 68  | GDMA Controller (GDMA)   | GDMA_IN_CH2_INTR   | INTMTX_COREO_DMA_IN_CH2_INTR_MAP_REG                                                                                | 4   |                                                    |
| 69  | GDMA Controller (GDMA)   | GDMA_OUT_CHO_INTR  | INTMTX_COREO_DMA_OUT_CHO_INTR_MAP_REG                                                                               | 5   |                                                    |
| 70  | GDMA Controller (GDMA)   | GDMA_OUT_CH1_INTR  | INTMTX_COREO_DMA_OUT_CH1_INTR_MAP_REG                                                                                | 6   | INTMTX_COREO_INT_STATUS_2_REG                     |
| 71  | GDMA Controller (GDMA)   | GDMA_OUT_CH2_INTR  | INTMTX_COREO_DMA_OUT_CH2_INTR_MAP_REG                                                                                | 7   |                                                    |
| 72  | SPI Controller (SPI)     | GPSPI2_INTR        | INTMTX_COREO_GPSPI2_INTR_MAP_REG                                                                                     | 8   |                                                    |
| 73  | AES Accelerator (AES)    | AES_INTR           | INTMTX_COREO_AES_INTR_MAP_REG                                                                                        | 9   |                                                    |
| 74  | SHA Accelerator (SHA)    | SHA_INTR           | INTMTX_COREO_SHA_INTR_MAP_REG                                                                                        | 10  |                                                    |
| 75  | RSA Accelerator (RSA)    | RSA_INTR           | INTMTX_COREO_RSA_INTR_MAP_REG                                                                                        | 11  |                                                    |
| 76  | ECC Accelerator (ECC)    | ECC_INTR           | INTMTX_COREO_ECC_INTR_MAP_REG                                                                                        | 12  |                                                    |
```