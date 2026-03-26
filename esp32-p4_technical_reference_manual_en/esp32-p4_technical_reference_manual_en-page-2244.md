

```markdown
| Register                  | Field                                                                 | GP-SPI2 | GP-SPI3 | LP-SPI |
|----------------------------|------------------------------------------------------------------------|---------|---------|--------|
| DMA_INT_ENA_REG           | DMA_INFIFO_FULL_ERR_INT_ENA                                         | Y       | Y       | —      |
|                            | DMA_OUTFIFO_EMPTY_ERR_INT_ENA                                       | Y       | Y       | —      |
|                            | SLV_EX_QPI_INT_ENA                                                   | Y       | Y       | —      |
|                            | SLV_EN_QPI_INT_ENA                                                   | Y       | Y       | —      |
|                            | SLV_CMD7_INT_ENA                                                     | Y       | Y       | —      |
|                            | SLV_CMD8_INT_ENA                                                     | Y       | Y       | —      |
|                            | SLV_CMD9_INT_ENA                                                     | Y       | Y       | —      |
|                            | SLV_CMDA_INT_ENA                                                     | Y       | Y       | —      |
|                            | SLV_RD_DMA_DONE_INT_ENA                                              | Y       | Y       | —      |
|                            | SLV_WR_DMA_DONE_INT_ENA                                              | Y       | Y       | —      |
|                            | LP_SPI_WAKEUP_INT_ENA                                                | —       | —       | Y      |
|                            | DMA_SEG_TRANS_DONE_INT_ENA                                           | Y       | Y       | —      |
|                            | SPI_SEG_MAGIC_ERR_INT_ENA                                            | Y       | —       | —      |
| DMA_INT_CLR_REG           | DMA_INFIFO_FULL_ERR_INT_CLR                                         | Y       | Y       | —      |
|                            | DMA_OUTFIFO_EMPTY_ERR_INT_CLR                                       | Y       | Y       | —      |
|                            | SLV_EX_QPI_INT_CLR                                                    | Y       | Y       | —      |
|                            | SLV_EN_QPI_INT_CLR                                                    | Y       | Y       | —      |
|                            | SLV_CMD7_INT_CLR                                                      | Y       | Y       | —      |
|                            | SLV_CMD8_INT_CLR                                                      | Y       | Y       | —      |
|                            | SLV_CMD9_INT_CLR                                                      | Y       | Y       | —      |
|                            | SLV_CMDA_INT_CLR                                                      | Y       | Y       | —      |
|                            | SLV_RD_DMA_DONE_INT_CLR                                               | Y       | Y       | —      |
|                            | SLV_WR_DMA_DONE_INT_CLR                                               | Y       | Y       | —      |
|                            | LP_SPI_WAKEUP_INT_CLR                                                  | —       | —       | Y      |
|                            | DMA_SEG_TRANS_DONE_INT_CLR                                           | Y       | Y       | —      |
|                            | SPI_SEG_MAGIC_ERR_INT_CLR                                            | Y       | —       | —      |
| DMA_INT_RAW_REG           | DMA_INFIFO_FULL_ERR_INT_RAW                                         | Y       | —       | —      |
|                            | DMA_OUTFIFO_EMPTY_ERR_INT_RAW                                       | Y       | —       | —      |
|                            | SLV_EX_QPI_INT_RAW                                                    | Y       | —       | —      |
|                            | SLV_EN_QPI_INT_RAW                                                    | Y       | —       | —      |
|                            | SLV_CMD7_INT_RAW                                                      | Y       | —       | —      |
|                            | SLV_CMD8_INT_RAW                                                      | Y       | —       | —      |
|                            | SLV_CMD9_INT_RAW                                                      | Y       | —       | —      |
|                            | SLV_CMDA_INT_RAW                                                      | Y       | —       | —      |
|                            | SLV_RD_DMA_DONE_INT_RAW                                               | Y       | —       | —      |
|                            | SLV_WR_DMA_DONE_INT_RAW                                               | Y       | —       | —      |
|                            | LP_SPI_WAKEUP_INT_RAW                                                 | —       | —       | Y      |
|                            | DMA_SEG_TRANS_DONE_INT_RAW                                           | Y       | —       | —      |
|                            | SPI_SEG_MAGIC_ERR_INT_RAW                                            | Y       | —       | —      |
```