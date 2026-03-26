

```markdown
| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30  | Reset                               |                                                                             |
| 29  | H264_DMA_IN_DSCR_TASK_OVF_CHO_INT_CLR | Write 1 to clear H264_DMA_IN_DSCR_TASK_OVF_CHO_INT.                        |
| 28  | H264_DMA_IN_DONE_CHO_INT_CLR         | Write 1 to clear H264_DMA_IN_DONE_CHO_INT. (WT)                             |
| 27  | H264_DMA_IN_SUC_EOF_CHO_INT_CLR      | Write 1 to clear H264_DMA_IN_SUC_EOF_CHO_INT. (WT)                          |
| 26  | H264_DMA_IN_ERR_EOF_CHO_INT_CLR      | Write 1 to clear H264_DMA_IN_ERR_EOF_CHO_INT. (WT)                          |
| 25  | H264_DMA_IN_DSCR_ERR_CHO_INT_CLR     | Write 1 to clear H264_DMA_IN_DSCR_ERR_CHO_INT. (WT)                         |
| 24  | H264_DMA_INFIFO_OVF_L1_CHO_INT_CLR   | Write 1 to clear H264_DMA_INFIFO_OVF_L1_CHO_INT. (WT)                       |
| 23  | H264_DMA_INFIFO_UDF_L1_CHO_INT_CLR   | Write 1 to clear H264_DMA_INFIFO_UDF_L1_CHO_INT. (WT)                       |
| 22  | H264_DMA_INFIFO_OVF_L2_CHO_INT_CLR   | Write 1 to clear H264_DMA_INFIFO_OVF_L2_CHO_INT. (WT)                       |
| 21  | H264_DMA_INFIFO_UDF_L2_CHO_INT_CLR   | Write 1 to clear H264_DMA_INFIFO_UDF_L2_CHO_INT. (WT)                       |
| 20  | H264_DMA_IN_DSCR_EMPTY_CHO_INT_CLR   | Write 1 to clear H264_DMA_IN_DSCR_EMPTY_CHO_INT. (WT)                       |
| 19  | H264_DMA_IN_DSCR_TASK_OVF_CHO_INT_CLR | Write 1 to clear H264_DMA_IN_DSCR_TASK_OVF_CHO_INT. (WT)                   |

Register 39.153. H264_DMA_IN_INT_CLR_CHO_REG (0x0510)
```