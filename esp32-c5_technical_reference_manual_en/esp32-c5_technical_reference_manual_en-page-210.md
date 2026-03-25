

```markdown
Register 5.7. AHB_DMA_OUT_INT_ENA_CHn_REG (n: 0-2) (0x0038+0x10*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 7   | AHB_DMA_OUT_DONE_CHn_INT_ENA               | Write 1 to enable AHB_DMA_OUT_DONE_CHn_INT. (R/W)                           |
| 6   | AHB_DMA_OUT_EOF_CHn_INT_ENA                | Write 1 to enable AHB_DMA_OUT_EOF_CHn_INT. (R/W)                            |
| 5   | AHB_DMA_OUT_DSCR_ERR_CHn_INT_ENA           | Write 1 to enable AHB_DMA_OUT_DSCR_ERR_CHn_INT. (R/W)                       |
| 4   | AHB_DMA_OUT_TOTAL_EOF_CHn_INT_ENA          | Write 1 to enable AHB_DMA_OUT_TOTAL_EOF_CHn_INT. (R/W)                      |
| 3   | AHB_DMA_OUTFIFO_OVF_CHn_INT_ENA            | Write 1 to enable AHB_DMA_OUTFIFO_OVF_CHn_INT. (R/W)                        |
| 2   | AHB_DMA_OUTFIFO_UDF_CHn_INT_ENA            | Write 1 to enable AHB_DMA_OUTFIFO_UDF_CHn_INT. (R/W)                        |
| 1   | AHB_DMA_OUT_RESP_ERR_CHn_INT_ENA           | Write 1 to enable AHB_DMA_OUT_RESP_ERR_CHn_INT. (R/W)                       |
| 0   | Reset                                      |                                                                             |
```