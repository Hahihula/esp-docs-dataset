

```markdown
Register 5.6. AHB_DMA_OUT_INT_ST_CHn_REG (n: 0-2) (0x0034+0x10*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                     |
| 30  | AHB_DMA_OUT_DONE_CHn_INT_ST                                                |
|     | The masked interrupt status of AHB_DMA_OUT_DONE_CHn_INT. (RO)                |
| 29  | AHB_DMA_OUT_EOF_CHn_INT_ST                                                 |
|     | The masked interrupt status of AHB_DMA_OUT_EOF_CHn_INT. (RO)                 |
| 28  | AHB_DMA_OUT_DSCR_ERR_CHn_INT_ST                                            |
|     | The masked interrupt status of AHB_DMA_OUT_DSCR_ERR_CHn_INT. (RO)            |
| 27  | AHB_DMA_OUT_TOTAL_EOF_CHn_INT_ST                                           |
|     | The masked interrupt status of AHB_DMA_OUT_TOTAL_EOF_CHn_INT. (RO)           |
| 26  | AHB_DMA_OUTFIFO_OVF_CHn_INT_ST                                            |
|     | The masked interrupt status of AHB_DMA_OUTFIFO_OVF_CHn_INT. (RO)             |
| 25  | AHB_DMA_OUTFIFO_UDF_CHn_INT_ST                                            |
|     | The masked interrupt status of AHB_DMA_OUTFIFO_UDF_CHn_INT. (RO)             |
| 24  | AHB_DMA_OUT_RESP_ERR_CHn_INT_ST                                           |
|     | The masked interrupt status of AHB_DMA_OUT_RESP_ERR_CHn_INT. (RO)            |
```