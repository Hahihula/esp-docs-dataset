

```markdown
Register 39.135. H264_DMA_OUT_INT_ENA_CH1_REG (0x0108)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | (reserved)                                                                  |
| 30  |                                             | Reset                                                                       |
| 29  | H264_DMA_OUT_DONE_CH1_INT_ENA              | Write 1 to enable H264_DMA_OUT_DONE_CH1_INT. (R/W)                          |
| 28  | H264_DMA_OUT_EOF_CH1_INT_ENA               | Write 1 to enable H264_DMA_OUT_EOF_CH1_INT. (R/W)                           |
| 27  | H264_DMA_OUT_DSCR_ERR_CH1_INT_ENA          | Write 1 to enable H264_DMA_OUT_DSCR_ERR_CH1_INT. (R/W)                      |
| 26  | H264_DMA_OUT_TOTAL_EOF_CH1_INT_ENA         | Write 1 to enable H264_DMA_OUT_TOTAL_EOF_CH1_INT. (R/W)                     |
| 25  | H264_DMA_OUTFIFO_OVF_L1_CH1_INT_ENA        | Write 1 to enable H264_DMA_OUTFIFO_OVF_L1_CH1_INT. (R/W)                    |
| 24  | H264_DMA_OUTFIFO_UDF_L1_CH1_INT_ENA        | Write 1 to enable H264_DMA_OUTFIFO_UDF_L1_CH1_INT. (R/W)                    |
| 23  | H264_DMA_OUTFIFO_OVF_L2_CH1_INT_ENA        | Write 1 to enable H264_DMA_OUTFIFO_OVF_L2_CH1_INT. (R/W)                    |
| 22  | H264_DMA_OUTFIFO_UDF_L2_CH1_INT_ENA        | Write 1 to enable H264_DMA_OUTFIFO_UDF_L2_CH1_INT. (R/W)                    |
| 21  |                                             |                                                                             |
| 20  | H264_DMA_OUT_DSCR_TASK_OVF_CH1_INT_ENA     | Write 1 to enable H264_DMA_OUT_DSCR_TASK_OVF_CH1_INT. (R/W)                 |

Espressif Systems    1963
ESP32-P4 TRM
PRELIMINARY
```