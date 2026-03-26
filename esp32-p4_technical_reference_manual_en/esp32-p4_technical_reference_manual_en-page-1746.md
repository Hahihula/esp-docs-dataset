

```markdown
Register 36.154. CSI_BRIG_INT_CLR_REG (0x0020)

| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | Reset                                                                      |
| 29  | CSI_BRIG_DMA_CFG_HAS_UPDATED_INT_CLR                                       |
| 28  | CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT_CLR                                        |
| 27  | CSI_BRIG_DISCARD_INT_CLR                                                   |
| 26  | CSI_BRIG_CSI_BUF_OVERRUN_INT_CLR                                           |
| 25  | CSI_BRIG_VADR_NUM_LT_REAL_INT_CLR                                          |
| 24  | CSI_BRIG_VADR_NUM_GT_REAL_INT_CLR                                          |

CSI_BRIG_VADR_NUM_GT_REAL_INT_CLR Write 1 to clear CSI_BRIG_VADR_NUM_GT_REAL_INT. (WT)

CSI_BRIG_VADR_NUM_LT_REAL_INT_CLR Write 1 to clear CSI_BRIG_VADR_NUM_LT_REAL_INT. (WT)

CSI_BRIG_DISCARD_INT_CLR Write 1 to clear CSI_BRIG_DISCARD_INT. (WT)

CSI_BRIG_CSI_BUF_OVERRUN_INT_CLR Write 1 to clear CSI_BRIG_CSI_BUF_OVERRUN_INT. (WT)

CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT_CLR Write 1 to clear CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT. (WT)

CSI_BRIG_DMA_CFG_HAS_UPDATED_INT_CLR Write 1 to clear CSI_BRIG_DMA_CFG_HAS_UPDATED_INT. (WT)
```