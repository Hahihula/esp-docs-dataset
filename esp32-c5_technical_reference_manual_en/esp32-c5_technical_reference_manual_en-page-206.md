

```markdown
| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30-8| AHB_DMA_IN_DONE_CHn_INT_ENA               | Write 1 to enable AHB_DMA_IN_DONE_CHn_INT. (R/W)                            |
| 7   | AHB_DMA_IN_SUC_EOF_CHn_INT_ENA            | Write 1 to enable AHB_DMA_IN_SUC_EOF_CHn_INT. (R/W)                         |
| 6   | AHB_DMA_IN_ERR_EOF_CHn_INT_ENA            | Write 1 to enable AHB_DMA_IN_ERR_EOF_CHn_INT. (R/W)                         |
| 5   | AHB_DMA_IN_DSCR_ERR_CHn_INT_ENA           | Write 1 to enable AHB_DMA_IN_DSCR_ERR_CHn_INT. (R/W)                        |
| 4   | AHB_DMA_IN_DSCR_EMPTY_CHn_INT_ENA         | Write 1 to enable AHB_DMA_IN_DSCR_EMPTY_CHn_INT. (R/W)                      |
| 3   | AHB_DMA_INFIFO_OVF_CHn_INT_ENA            | Write 1 to enable AHB_DMA_INFIFO_OVF_CHn_INT. (R/W)                         |
| 2   | AHB_DMA_INFIFO_UDF_CHn_INT_ENA            | Write 1 to enable AHB_DMA_INFIFO_UDF_CHn_INT. (R/W)                         |
| 1   | AHB_DMA_IN_RESP_ERR_CHn_INT_ENA           | Write 1 to enable AHB_DMA_IN_RESP_ERR_CHn_INT. (R/W)                        |
| 0   | Reset                                      |                                                                             |

Register 5.3. AHB_DMA_IN_INT_ENA_CHn_REG (n: 0-2) (0x0008+0x10*n)
```