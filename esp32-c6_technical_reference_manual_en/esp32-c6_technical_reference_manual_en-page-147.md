

```markdown
Register 4.3. GDMA_IN_INT_ENA_CHn_REG (n: 0-2) (0x0008+0x10*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 7   | GDMA_IN_DONE_CHn_INT_ENA      | Write 1 to enable GDMA_IN_DONE_CHn_INT. (R/W)                               |
| 6   | GDMA_IN_SUC_EOF_CHn_INT_ENA   | Write 1 to enable GDMA_IN_SUC_EOF_CHn_INT. (R/W)                            |
| 5   | GDMA_IN_ERR_EOF_CHn_INT_ENA   | Write 1 to enable GDMA_IN_ERR_EOF_CHn_INT. (R/W)                            |
| 4   | GDMA_IN_DSCR_ERR_CHn_INT_ENA  | Write 1 to enable GDMA_IN_DSCR_ERR_CHn_INT. (R/W)                           |
| 3   | GDMA_IN_DSCR_EMPTY_CHn_INT_ENA| Write 1 to enable GDMA_IN_DSCR_EMPTY_CHn_INT. (R/W)                         |
| 2   | GDMA_INFIFO_OVF_CHn_INT_ENA   | Write 1 to enable GDMA_INFIFO_OVF_CHn_INT. (R/W)                            |
| 1   | GDMA_INFIFO_UDF_CHn_INT_ENA   | Write 1 to enable GDMA_INFIFO_UDF_CHn_INT. (R/W)                            |
| 0   |                                | Reset                                                                       |
```