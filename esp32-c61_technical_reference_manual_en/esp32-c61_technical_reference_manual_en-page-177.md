

```markdown
## Register 3.8. AHB_DMA_OUT_INT_CLR_CHn_REG (n: 0-1) (0x003C+0x10*n)

```

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | (reserved)                                                                  |
| 30  | AHB_DMA_OUT_DONE_CHn_INT_CLR                | Write 1 to clear AHB_DMA_OUT_DONE_CHn_INT. (WT)                             |
| 29  | AHB_DMA_OUT_EOF_CHn_INT_CLR                 | Write 1 to clear AHB_DMA_OUT_EOF_CHn_INT. (WT)                              |
| 28  | AHB_DMA_OUT_DSCR_ERR_CHn_INT_CLR            | Write 1 to clear AHB_DMA_OUT_DSCR_ERR_CHn_INT. (WT)                         |
| 27  | AHB_DMA_OUT_TOTAL_EOF_CHn_INT_CLR           | Write 1 to clear AHB_DMA_OUT_TOTAL_EOF_CHn_INT. (WT)                        |
| 26  | AHB_DMA_OUTFIFO_OVF_CHn_INT_CLR             | Write 1 to clear AHB_DMA_OUTFIFO_OVF_CHn_INT. (WT)                          |
| 25  | AHB_DMA_OUTFIFO_UDF_CHn_INT_CLR             | Write 1 to clear AHB_DMA_OUTFIFO_UDF_CHn_INT. (WT)                          |

```
Espressif Systems
177
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```