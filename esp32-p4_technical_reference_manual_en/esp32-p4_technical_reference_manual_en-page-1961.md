
```markdown
| Chapter 39 H264 Encoder                                                                 GoBack |
|------------------------------------------------------------------------------------------|
| Register 39.133. H264_DMA_OUT_INT_CLR_CHO_REG (0x0010)                                   |
|                                                                                        |
| (reserved)                                                                              |
|                                                                                        |
| 31         9   8   7   6   5   4   3   2   1   0                                         |
| 0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   Reset    |
|                                                                                        |
| H264_DMA_OUT_DONE_CHO_INT_CLR Write 1 to clear H264_DMA_OUT_DONE_CHO_INT. (WT)           |
| H264_DMA_OUT_EOF_CHO_INT_CLR Write 1 to clear H264_DMA_OUT_EOF_CHO_INT. (WT)             |
| H264_DMA_OUT_DSCR_ERR_CHO_INT_CLR Write 1 to clear H264_DMA_OUT_DSCR_ERR_CHO_INT.       |
|                                                                                          |
| (WT)                                                                                    |
| H264_DMA_OUT_TOTAL_EOF_CHO_INT_CLR Write 1 to clear H264_DMA_OUT_TOTAL_EOF_CHO_INT.     |
|                                                                                          |
| (WT)                                                                                    |
| H264_DMA_OUTFIFO_OVF_L1_CHO_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_OVF_L1_CHO_INT.    |
|                                                                                          |
| (WT)                                                                                    |
| H264_DMA_OUTFIFO_UDF_L1_CHO_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_UDF_L1_CHO_INT.    |
|                                                                                          |
| (WT)                                                                                    |
| H264_DMA_OUTFIFO_OVF_L2_CHO_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_OVF_L2_CHO_INT.    |
|                                                                                          |
| (WT)                                                                                    |
| H264_DMA_OUTFIFO_UDF_L2_CHO_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_UDF_L2_CHO_INT.    |
|                                                                                          |
| (WT)                                                                                    |
| H264_DMA_OUT_DSCR_TASK_OVF_CHO_INT_CLR Write 1 to clear H264_DMA_OUT_DSCR_TASK_OVF_CHO_INT.|
|(WT)                                                                                    |
```