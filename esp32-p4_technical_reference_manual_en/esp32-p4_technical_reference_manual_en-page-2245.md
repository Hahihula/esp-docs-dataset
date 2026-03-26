

```markdown
| Register                  | Field                                                                 | GP-SPI2 | GP-SPI3 | LP-SPI |
|----------------------------|------------------------------------------------------------------------|----------|----------|--------|
| DMA_INT_ST_REG            | DMA_INFIFO_FULL_ERR_INT_ST                                           | Y        | Y        | —      |
|                            | DMA_OUTFIFO_EMPTY_ERR_INT_ST                                         | Y        | Y        | —      |
|                            | SLV_EX_QPI_INT_ST                                                     | Y        | Y        | —      |
|                            | SLV_EN_QPI_INT_ST                                                     | Y        | Y        | —      |
|                            | SLV_CMD7_INT_ST                                                       | Y        | Y        | —      |
|                            | SLV_CMD8_INT_ST                                                       | Y        | Y        | —      |
|                            | SLV_CMD9_INT_ST                                                       | Y        | Y        | —      |
|                            | SLV_CMDA_INT_ST                                                       | Y        | Y        | —      |
|                            | SLV_RD_DMA_DONE_INT_ST                                                | Y        | Y        | —      |
|                            | SLV_WR_DMA_DONE_INT_ST                                                | Y        | Y        | —      |
|                            | LP_SPI_WAKEUP_INT_ST                                                  | —        | —        | Y      |
|                            | DMA_SEG_TRANS_DONE_INT_ST                                             | Y        | —        | —      |
|                            | SPI_SEG_MAGIC_ERR_INT_ST                                              | Y        | —        | —      |
|                            | DMA_INFIFO_FULL_ERR_INT_ST                                            | Y        | Y        | —      |
|                            | DMA_OUTFIFO_EMPTY_ERR_INT_ST                                         | Y        | Y        | —      |
|                            | SLV_EX_QPI_INT_ST                                                     | Y        | Y        | —      |
|                            | SLV_EN_QPI_INT_ST                                                     | Y        | Y        | —      |
|                            | SLV_CMD7_INT_ST                                                       | Y        | Y        | —      |
|                            | SLV_CMD8_INT_ST                                                       | Y        | Y        | —      |
|                            | SLV_CMD9_INT_ST                                                       | Y        | Y        | —      |
| DMA_INT_SET_REG           | SLV_CMDA_INT_ST                                                       | Y        | Y        | —      |
|                            | SLV_RD_DMA_DONE_INT_ST                                                | Y        | Y        | —      |
|                            | SLV_WR_DMA_DONE_INT_ST                                                | Y        | Y        | —      |
|                            | LP_SPI_WAKEUP_INT_ST                                                  | —        | —        | Y      |
|                            | DMA_SEG_TRANS_DONE_INT_ST                                             | Y        | Y        | —      |
|                            | SPI_SEG_MAGIC_ERR_INT_ST                                              | Y        | —        | —      |

## 43.10.3 Interrupt Differences

Table 43.10-3 lists the interrupts supported in GP-SPI2, GP-SPI3, and LP-SPI.

**Table 43.10-3. Interrupt Differences**

| Interrupt                                 | GP-SPI2 | GP-SPI3 | LP-SPI |
|--------------------------------------------|---------|---------|--------|
| SPI_DMA_INFIFO_FULL_ERR_INT               | Y       | Y       | —      |
| SPI_DMA_OUTFIFO_EMPTY_ERR_INT             | Y       | Y       | —      |
| SPI_SLV_EX_QPI_INT                        | Y       | Y       | —      |
| SPI_SLV_EN_QPI_INT                        | Y       | Y       | —      |
| SPI_SLV_CMD7_INT                          | Y       | Y       | —      |
| SPI_SLV_CMD8_INT                          | Y       | Y       | —      |
| SPI_SLV_CMD9_INT                          | Y       | Y       | —      |
| SPI_SLV_CMDA_INT                          | Y       | Y       | —      |
```