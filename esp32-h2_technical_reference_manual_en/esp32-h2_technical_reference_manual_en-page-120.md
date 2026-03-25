

```markdown
Register 3.3. GDMA_IN_INT_ENA_CHn_REG (n: 0-2) (0x0008+0x10*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 7   | GDMA_INFIFO_OVF_CHO_INT_ENA                                                 |
| 6   | GDMA_INFIFO_UDF_CHO_INT_ENA                                                 |
| 5   | GDMA_IN_DSCR_ERR_EOF_CHn_INT_ENA                                            |
| 4   | GDMA_IN_SUC_EOF_CHn_INT_ENA                                                 |
| 3   | GDMA_IN_DONE_CHn_INT_ENA                                                    |
| 2   | Reset                                                                       |
| 1   | (reserved)                                                                  |
| 0   | (reserved)                                                                  |

GDMA_IN_DONE_CHn_INT_ENA    Write 1 to enable GDMA_IN_DONE_CHn_INT. (R/W)
GDMA_IN_SUC_EOF_CHn_INT_ENA  Write 1 to enable GDMA_IN_SUC_EOF_CHn_INT. (R/W)
GDMA_IN_ERR_EOF_CHn_INT_ENA  Write 1 to enable GDMA_IN_ERR_EOF_CHn_INT. (R/W)
GDMA_IN_DSCR_ERR_CHn_INT_ENA Write 1 to enable GDMA_IN_DSCR_ERR_CHn_INT. (R/W)
GDMA_IN_DSCR_EMPTY_CHn_INT_ENA Write 1 to enable GDMA_IN_DSCR_EMPTY_CHn_INT. (R/W)
GDMA_INFIFO_OVF_CHn_INT_ENA   Write 1 to enable GDMA_INFIFO_OVF_CHn_INT. (R/W)
GDMA_INFIFO_UDF_CHn_INT_ENA   Write 1 to enable GDMA_INFIFO_UDF_CHn_INT. (R/W)
```