

```markdown
|31|10|9|8|7|6|5|4|3|2|1|0|
|:------------------------------------------------------------------------|:-----|:-----------------------------|:----------|:--------------------------------------------|:-----------|:---------|:-------|:------|:----|:---|
||Reset|(reserved)|H264_DMA_IN_DSCR_TASK_OVF_CH1_INT_ST|                                    |                                    |                                    |                                    |                                    |                                    |
||||H264_DMA_IN_DSCR_ERR_CH1_INT_ST|                                    |                                    |                                    |                                    |                                    |                                    |
|||||H264_DMA_IN_INFIFO_OVF_L1_CH1_INT_ST|                                    |                                    |                                    |                                    |                                    |
||||||H264_DMA_IN_INFIFO_UDF_L1_CH1_INT_ST|                                    |                                    |                                    |                                    |
|||||||H264_DMA_IN_INFIFO_OVF_L2_CH1_INT_ST|                                    |                                    |                                    |                                    |
||||||||H264_DMA_IN_INFIFO_UDF_L2_CH1_INT_ST|                                    |                                    |                                    |                                    |
||||||||||H264_DMA_IN_DSCR_EMPTY_CH1_INT_ST|                                    |                                    |                                    |                                    |
||||||||||||H264_DMA_IN_DSCR_TASK_OVF_CH1_INT_ST|
```

Register 39.156. H264_DMA_IN_INT_ST_CH1_REG (0x060C)

```markdown
H264_DMA_IN_DONE_CH1_INT_ST The masked interrupt status of  
H264_DMA_IN_DONE_CH1_INT. (RO)  

H264_DMA_IN_SUC_EOF_CH1_INT_ST The masked interrupt status of  
H264_DMA_IN_SUC_EOF_CH1_INT. (RO)  

H264_DMA_IN_ERR_EOF_CH1_INT_ST The masked interrupt status of  
H264_DMA_IN_ERR_EOF_CH1_INT. (RO)  

H264_DMA_IN_DSCR_ERR_CH1_INT_ST The masked interrupt status of  
H264_DMA_IN_DSCR_ERR_CH1_INT. (RO)  

H264_DMA_INFIFO_OVF_L1_CH1_INT_ST The masked interrupt status of  
H264_DMA_INFIFO_OVF_L1_CH1_INT. (RO)  

H264_DMA_INFIFO_UDF_L1_CH1_INT_ST The masked interrupt status of  
H264_DMA_INFIFO_UDF_L1_CH1_INT. (RO)  

H264_DMA_INFIFO_OVF_L2_CH1_INT_ST The masked interrupt status of  
H264_DMA_INFIFO_OVF_L2_CH1_INT. (RO)  

H264_DMA_INFIFO_UDF_L2_CH1_INT_ST The masked interrupt status of  
H264_DMA_INFIFO_UDF_L2_CH1_INT. (RO)  

H264_DMA_IN_DSCR_EMPTY_CH1_INT_ST The masked interrupt status of  
H264_DMA_IN_DSCR_EMPTY_CH1_INT. (RO)  

H264_DMA_IN_DSCR_TASK_OVF_CH1_INT_ST The masked interrupt status of  
H264_DMA_IN_DSCR_TASK_OVF_CH1_INT. (RO)
```