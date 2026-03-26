

```markdown
Register 39.161. H264_DMA_IN_INT_CLR_CH2_REG (0x0710)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | (reserved)                                                                  |
| 30  |                                             | Reset                                                                       |
| 29  | H264_DMA_IN_DSCR_TASK_OVF_CH2_INT_CLR       | Write 1 to clear H264_DMA_IN_DSCR_TASK_OVF_CH2_INT.                        |
| 28  | H264_DMA_IN_SUC_EOF_CH2_INT_CLR             | Write 1 to clear H264_DMA_IN_SUC_EOF_CH2_INT.                              |
| 27  | H264_DMA_IN_ERR_EOF_CH2_INT_CLR             | Write 1 to clear H264_DMA_IN_ERR_EOF_CH2_INT. (WT)                          |
| 26  | H264_DMA_IN_DSCR_ERR_CH2_INT_CLR            | Write 1 to clear H264_DMA_IN_DSCR_ERR_CH2_INT. (WT)                         |
| 25  | H264_DMA_INFIFO_OVF_L1_CH2_INT_CLR          | Write 1 to clear H264_DMA_INFIFO_OVF_L1_CH2_INT.                            |
| 24  | H264_DMA_INFIFO_UDF_L1_CH2_INT_CLR          | Write 1 to clear H264_DMA_INFIFO_UDF_L1_CH2_INT.                            |
| 23  | H264_DMA_INFIFO_OVF_L2_CH2_INT_CLR          | Write 1 to clear H264_DMA_INFIFO_OVF_L2_CH2_INT.                            |
| 22  | H264_DMA_INFIFO_UDF_L2_CH2_INT_CLR          | Write 1 to clear H264_DMA_INFIFO_UDF_L2_CH2_INT.                            |
| 21  | H264_DMA_IN_DSCR_EMPTY_CH2_INT_CLR          | Write 1 to clear H264_DMA_IN_DSCR_EMPTY_CH2_INT. (WT)                       |
| 20  | H264_DMA_IN_DSCR_TASK_OVF_CH2_INT_CLR       | Write 1 to clear H264_DMA_IN_DSCR_TASK_OVF_CH2_INT. (WT)                    |

Espressif Systems    1989    ESP32-P4 TRM
Submit Documentation Feedback PRELIMINARY
```