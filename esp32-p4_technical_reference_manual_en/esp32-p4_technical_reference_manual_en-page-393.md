

```markdown
Chapter 5 VDMA Controller (VDMA)

Register 5.26. DMAC_CHn_INTCLEARO_REG (n: 1-4) (0x0100*n + 0x0198)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0                                                                             |
| 30  | 0                                                                             |
| 29  | 0                                                                             |
| 28  | 0                                                                             |
| 27  | DMAC_CHn_CLEAR_BLOCK_TFR_DONE_INTSTAT (WO)                                 |
| 26  | DMAC_CHn_CLEAR_DST_DEC_ERR_INTSTAT                                        |
| 25  | DMAC_CHn_CLEAR_DST_SLV_ERR_INTSTAT                                       |
| 24  | DMAC_CHn_CLEAR_LLI_WR_DEC_ERR_INTSTAT                                    |
| 23  | DMAC_CHn_CLEAR_LLI_RD_DEC_ERR_INTSTAT                                   |
| 22  | DMAC_CHn_CLEAR_SRC_SLV_ERR_INTSTAT                                      |
| 21  | DMAC_CHn_CLEAR_SRC_DEC_ERR_INTSTAT                                     |
| 20  | DMAC_CHn_CLEAR_DST_TRANSCOMP_INTSTAT                                    |
| 19  | DMAC_CHn_CLEAR_SRC_TRANSCOMP_INTSTAT                                   |
| 18  | DMAC_CHn_DMA_TFR_DONE_INTSTAT                                           |
| 17  | DMAC_CHn_ABORTED_INTSTAT                                                 |
| 16  | DMAC_CHn_DISABLED_INTSTAT                                                |
| 15  | DMAC_CHn_SUSPENDED_INTSTAT                                               |
| 14  | DMAC_CHn_SRC_SUSPENDED_INTSTAT                                          |
| 13  | DMAC_CHn_WRONCH_ERR_INTSTAT                                              |
| 12  | DMAC_CHn_SHADOWREG_WR_VALID_INTSTAT                                     |
| 11  | DMAC_CHn_RODERR_WR_INTSTAT                                               |
| 10  | DMAC_CHn_WRPERR_INTSTAT                                                  |
| 9   | DMAC_CHn_DEC_ERR_INTSTAT                                                 |
| 8   | DMAC_CHn_MULTIBLTYPE_ERR_INTSTAT                                        |
| 7   | DMAC_CHn_LLI_WR_OR_SLV_ERR_INTSTAT                                     |
| 6   | DMAC_CHn_LLI_RD_ERR_INTSTAT                                              |
| 5   | DMAC_CHn_SRC_SIV_ERR_INTSTAT                                            |
| 4   | DMAC_CHn_DST_SIV_ERR_INTSTAT                                            |
| 3   | DMAC_CHn_SRC_DEC_ERR_INTSTAT                                            |
| 2   | DMAC_CHn_DST_DEC_ERR_INTSTAT                                            |
| 1   | DMAC_CHn_SRC_TRANSCOMP_INTSTAT                                          |
| 0   | DMAC_CHn_DST_TRANSCOMP_INTSTAT                                          |

DMAC_CHn_CLEAR_BLOCK_TFR_DONE_INTSTAT Write 1 to clear DMAC_CHn_BLOCK_TFR_DONE_INTSTAT. (WO)

DMAC_CHn_CLEAR_DMA_TFR_DONE_INTSTAT Write 1 to clear DMAC_CHn_DMA_TFR_DONE_INTSTAT. (WO)

DMAC_CHn_CLEAR_SRC_TRANSCOMP_INTSTAT Write 1 to clear DMAC_CHn_SRC_TRANSCOMP_INTSTAT. (WO)

DMAC_CHn_CLEAR_DST_TRANSCOMP_INTSTAT Write 1 to clear DMAC_CHn_DST_TRANSCOMP_INTSTAT. (WO)

DMAC_CHn_CLEAR_SRC_DEC_ERR_INTSTAT Write 1 to clear DMAC_CHn_SRC_DEC_ERR_INTSTAT. (WO)

DMAC_CHn_CLEAR_DST_DEC_ERR_INTSTAT Write 1 to clear DMAC_CHn_DST_DEC_ERR_INTSTAT. (WO)

DMAC_CHn_CLEAR_SRC_SLV_ERR_INTSTAT Write 1 to clear DMAC_CHn_SRC_SLV_ERR_INTSTAT. (WO)

DMAC_CHn_CLEAR_DST_SLV_ERR_INTSTAT Write 1 to clear DMAC_CHn_DST_SLV_ERR_INTSTAT. (WO)

DMAC_CHn_CLEAR_LLI_RD_DEC_ERR_INTSTAT Write 1 to clear DMAC_CHn_LLI_RD_DEC_ERR_INTSTAT. (WO)

DMAC_CHn_CLEAR_LLI_WR_DEC_ERR_INTSTAT Write 1 to clear DMAC_CHn_LLI_WR_DEC_ERR_INTSTAT. (WO)

Continued on the next page...
```