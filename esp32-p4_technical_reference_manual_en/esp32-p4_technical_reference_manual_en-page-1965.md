
```markdown
| Chapter 39 H264 Encoder | GoBack |
|--------------------------|--------|
| Register 39.137. H264_DMA_OUT_INT_CLR_CH1_REG (0x0110) |

```
```plaintext
(reserved)
H264_DMA_OUT_DONE_CH1_INT_CLR Write 1 to clear H264_DMA_OUT_DONE_CH1_INT. (WT)

H264_DMA_OUT_EOF_CH1_INT_CLR Write 1 to clear H264_DMA_OUT_EOF_CH1_INT. (WT)

H264_DMA_OUT_DSCR_ERR_CH1_INT_CLR Write 1 to clear H264_DMA_OUT_DSCR_ERR_CH1_INT. (WT)

H264_DMA_OUT_TOTAL_EOF_CH1_INT_CLR Write 1 to clear H264_DMA_OUT_TOTAL_EOF_CH1_INT. (WT)

H264_DMA_OUTFIFO_OVF_L1_CH1_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_OVF_L1_CH1_INT. (WT)

H264_DMA_OUTFIFO_UDF_L1_CH1_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_UDF_L1_CH1_INT. (WT)

H264_DMA_OUTFIFO_OVF_L2_CH1_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_OVF_L2_CH1_INT. (WT)

H264_DMA_OUTFIFO_UDF_L2_CH1_INT_CLR Write 1 to clear H264_DMA_OUTFIFO_UDF_L2_CH1_INT. (WT)

H264_DMA_OUT_DSCR_TASK_OVF_CH1_INT_CLR Write 1 to clear H264_DMA_OUT_DSCR_TASK_OVF_CH1_INT. (WT)
```
```plaintext
31 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0
--+---+---+---+---+---+---+---+---+---+---+
0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 Reset
```