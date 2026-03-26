
```markdown
| Chapter 39 H264 Encoder | GoBack |
|--------------------------|--------|
| Register 39.134. H264_DMA_OUT_INT_RAW_CH1_REG (0x0104) |          |

| Bit Position | Description                                                                 | Reset Value |
|--------------|-----------------------------------------------------------------------------|-----------|
| 31           | (reserved)                                                                  | 0         |
| 30-9         | (reserved)                                                                  | 0         |
| 8            | H264_DMA_OUT_DONE_CH1_INT_RAW The raw interrupt status of H264_DMA_OUT_DONE_CH1_INT. (R/WTC/SS) | 0         |
| 7            | H264_DMA_OUT_EOF_CH1_INT_RAW The raw interrupt status of H264_DMA_OUT_EOF_CH1_INT. (R/WTC/SS) | 0         |
| 6            | H264_DMA_OUT_DSCR_ERR_CH1_INT_RAW The raw interrupt status of H264_DMA_OUT_DSCR_ERR_CH1_INT. (R/WTC/SS) | 0         |
| 5            | H264_DMA_OUT_TOTAL_EOF_CH1_INT_RAW The raw interrupt status of H264_DMA_OUT_TOTAL_EOF_CH1_INT. (R/WTC/SS) | 0         |
| 4            | H264_DMA_OUTFIFO_OVF_L1_CH1_INT_RAW The raw interrupt status of H264_DMA_OUTFIFO_OVF_L1_CH1_INT. (R/WTC/SS) | 0         |
| 3            | H264_DMA_OUTFIFO_UDF_L1_CH1_INT_RAW The raw interrupt status of H264_DMA_OUTFIFO_UDF_L1_CH1_INT. (R/WTC/SS) | 0         |
| 2            | H264_DMA_OUTFIFO_OVF_L2_CH1_INT_RAW The raw interrupt status of H264_DMA_OUTFIFO_OVF_L2_CH1_INT. (R/WTC/SS) | 0         |
| 1            | H264_DMA_OUTFIFO_UDF_L2_CH1_INT_RAW The raw interrupt status of H264_DMA_OUTFIFO_UDF_L2_CH1_INT. (R/WTC/SS) | 0         |
| 0            | H264_DMA_OUT_DSCR_TASK_OVF_CH1_INT_RAW The raw interrupt status of H264_DMA_OUT_DSCR_TASK_OVF_CH1_INT. (R/WTC/SS) | 0         |

Espressif Systems
1962
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```