

```markdown
Chapter 39 H264 Encoder

Register 39.173. H264_DMA_IN_INT_CLR_CH5_REG (0x0A1C)

(reserved)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     | H264_DMA_FETCH_MB_COL_CNT_OVF_CH5_INT_CLR |
|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     | H264_DMA_INFIFO_OVF_L1_CH5_INT_CLR |
|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     | H264_DMA_INFIFO_UDF_L1_CH5_INT_CLR |
|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     | H264_DMA_IN_DONE_CH5_INT_CLR |
|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     | H264_DMA_IN_SUC_EOF_CH5_INT_CLR |

H264_DMA_IN_DONE_CH5_INT_CLR Write 1 to clear H264_DMA_IN_DONE_CH5_INT. (WT)

H264_DMA_IN_SUC_EOF_CH5_INT_CLR Write 1 to clear H264_DMA_IN_SUC_EOF_CH5_INT. (WT)

H264_DMA_INFIFO_OVF_L1_CH5_INT_CLR Write 1 to clear H264_DMA_INFIFO_OVF_L1_CH5_INT. (WT)

H264_DMA_INFIFO_UDF_L1_CH5_INT_CLR Write 1 to clear H264_DMA_INFIFO_UDF_L1_CH5_INT. (WT)

H264_DMA_FETCH_MB_COL_CNT_OVF_CH5_INT_CLR Write 1 to clear H264_DMA_FETCH_MB_COL_CNT_OVF_CH5. (WT)
```