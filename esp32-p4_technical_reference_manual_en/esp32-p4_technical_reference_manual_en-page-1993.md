

```markdown
| Bit (reserved) | H264_DMA_IN_DSCR_TASK_OVF_CH3_INT_CLR | H264_DMA_IN_DSCR_EMPTY_CH3_INT_CLR | H264_DMA_IN_INFIFO_OVF_L1_CH3_INT_CLR | H264_DMA_IN_INFIFO_UF_L1_CH3_INT_CLR | H264_DMA_IN_INFIFO_OVF_L2_CH3_INT_CLR | H264_DMA_IN_INFIFO_UF_L2_CH3_INT_CLR | H264_DMA_IN_DSCR_EMPTY_CH3_INT_CLR | H264_DMA_IN_SUC_EOF_CH3_INT_CLR | H264_DMA_IN_ERR_EOF_CH3_INT_CLR | H264_DMA_IN_ERR_CH3_INT_CLR | H264_DMA_IN_DSCR_ERR_CH3_INT_CLR |
|----------------|----------------------------------------|-------------------------------------|-----------------------------------------|---------------------------------------|-----------------------------------------|---------------------------------------|--------------------------------------|----------------------------------|---------------------------------|-------------------------------|--------------------------------|
| 31             |                                        |                                     |                                         |                                       |                                         |                                       |                                      |                                  |                                 |                               |                                |
|                |                                        |                                     |                                         |                                       |                                         |                                       |                                      |                                  |                                 |                               |                                |
| Reset          |                                        |                                     |                                         |                                       |                                         |                                       |                                      |                                  |                                 |                               |                                |

H264_DMA_IN_DONE_CH3_INT_CLR  Write 1 to clear H264_DMA_IN_DONE_CH3_INT. (WT)

H264_DMA_IN_SUC_EOF_CH3_INT_CLR  Write 1 to clear H264_DMA_IN_SUC_EOF_CH3_INT. (WT)

H264_DMA_IN_ERR_EOF_CH3_INT_CLR  Write 1 to clear H264_DMA_IN_ERR_EOF_CH3_INT. (WT)

H264_DMA_IN_DSCR_ERR_CH3_INT_CLR  Write 1 to clear H264_DMA_IN_DSCR_ERR_CH3_INT. (WT)

H264_DMA_INFIFO_OVF_L1_CH3_INT_CLR  Write 1 to clear H264_DMA_INFIFO_OVF_L1_CH3_INT. (WT)

H264_DMA_INFIFO_UF_L1_CH3_INT_CLR  Write 1 to clear H264_DMA_INFIFO_UF_L1_CH3_INT. (WT)

H264_DMA_INFIFO_OVF_L2_CH3_INT_CLR  Write 1 to clear H264_DMA_INFIFO_OVF_L2_CH3_INT. (WT)

H264_DMA_INFIFO_UF_L2_CH3_INT_CLR  Write 1 to clear H264_DMA_INFIFO_UF_L2_CH3_INT. (WT)

H264_DMA_IN_DSCR_EMPTY_CH3_INT_CLR  Write 1 to clear H264_DMA_IN_DSCR_EMPTY_CH3_INT. (WT)

H264_DMA_IN_DSCR_TASK_OVF_CH3_INT_CLR  Write 1 to clear H264_DMA_IN_DSCR_TASK_OVF_CH3_INT. (WT)
```