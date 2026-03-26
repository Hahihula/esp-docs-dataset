

```markdown
Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI)

Register 4.4. AHB_DMA_IN_INT_CLR_CHn_REG (n: 0-2) (0x000C+0x10*n)
```

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | AHB_DMA_IN_RESP_ERR_CHn_INT_CLR            | Write 1 to clear AHB_DMA_IN_RESP_ERR_CHn_INT. (WT)                          |
| 29  | AHB_DMA_IN_INFIFO_UDF_CHn_INT_CLR          | Write 1 to clear AHB_DMA_IN_INFIFO_UDF_CHn_INT. (WT)                        |
| 28  | AHB_DMA_IN_DSCR_ERR_CHn_INT_CLR            | Write 1 to clear AHB_DMA_IN_DSCR_ERR_CHn_INT. (WT)                          |
| 27  | AHB_DMA_IN_ERR_EOF_CHn_INT_CLR             | Write 1 to clear AHB_DMA_IN_ERR_EOF_CHn_INT. (WT)                           |
| 26  | AHB_DMA_IN_SUC_EOF_CHn_INT_CLR             | Write 1 to clear AHB_DMA_IN_SUC_EOF_CHn_INT. (WT)                           |
| 25  | AHB_DMA_IN_DONE_CHn_INT_CLR                | Write 1 to clear AHB_DMA_IN_DONE_CHn_INT. (WT)                              |

```markdown
AHB_DMA_IN_DONE_CHn_INT_CLR   Write 1 to clear AHB_DMA_IN_DONE_CHn_INT. (WT)
AHB_DMA_IN_SUC_EOF_CHn_INT_CLR Write 1 to clear AHB_DMA_IN_SUC_EOF_CHn_INT. (WT)
AHB_DMA_IN_ERR_EOF_CHn_INT_CLR Write 1 to clear AHB_DMA_IN_ERR_EOF_CHn_INT. (WT)
AHB_DMA_IN_DSCR_ERR_CHn_INT_CLR Write 1 to clear AHB_DMA_IN_DSCR_ERR_CHn_INT. (WT)
AHB_DMA_IN_DSCR_EMPTY_CHn_INT_CLR Write 1 to clear AHB_DMA_IN_DSCR_EMPTY_CHn_INT. (WT)
AHB_DMA_INFIFO_OVF_CHn_INT_CLR Write 1 to clear AHB_DMA_INFIFO_OVF_CHn_INT. (WT)
AHB_DMA_INFIFO_UDF_CHn_INT_CLR Write 1 to clear AHB_DMA_INFIFO_UDF_CHn_INT. (WT)
AHB_DMA_IN_RESP_ERR_CHn_INT_CLR Write 1 to clear AHB_DMA_IN_RESP_ERR_CHn_INT. (WT)
```

Espressif Systems
264
ESP32-P4 TRM
PRELIMINARY

Submit Documentation Feedback
```