

```markdown
Register 5.24. DMAC_Ch_n_INTSTATUSO_REG (n: 1-4) (0x0100*n + 0x0188)

DMAC_Ch_n_BLOCK_TFR_DONE_INTSTAT    Block transfer done status bit. (RO)
DMAC_Ch_n_DMA_TFR_DONE_INTSTAT      DMA transfer done status bit. (RO)
DMAC_Ch_n_SRC_TRANSCOMP_INTSTAT     Source DMA transfer completed status bit. (RO)
DMAC_Ch_n_DST_TRANSCOMP_INTSTAT     Destination DMA transfer completed status bit. (RO)
DMAC_Ch_n_SRC_DEC_ERR_INTSTAT       Source decode error status bit. The decode error is detected by the master interface during source transfer. (RO)
DMAC_Ch_n_DST_DEC_ERR_INTSTAT       Destination decode error status bit. The decode error is detected by the master interface during destination transfer. (RO)
DMAC_Ch_n_SRC_SLV_ERR_INTSTAT       Source slave error status bit. The slave error is detected by the master interface during source transfer. This error occurs if the slave interface that reads data issues a slave error. (RO)
DMAC_Ch_n_DST_SLV_ERR_INTSTAT       Destination slave error status bit. The slave error is detected by the master interface during source transfer. This error occurs if the slave interface that writes data issues a slave error. (RO)
DMAC_Ch_n_LLI_RD_DEC_ERR_INTSTAT    LLI read decode error status bit. The decode error is detected by the master interface during LLI read operation. (RO)
DMAC_Ch_n_LLI_WR_DEC_ERR_INTSTAT    LLI write decode error status bit. The decode error is detected by the master interface during LLI write-back operation. (RO)
DMAC_Ch_n_LLI_RD_SLV_ERR_INTSTAT    LLI read slave error status bit. The slave error is detected by the master interface during LLI read operation. (RO)
DMAC_Ch_n_LLI_WR_SLV_ERR_INTSTAT    LLI write slave error status bit. The slave error is detected by the master interface during LLI write-back operation. (RO)

Continued on the next page...
```