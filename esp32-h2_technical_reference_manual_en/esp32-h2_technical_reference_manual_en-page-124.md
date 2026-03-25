

```markdown
## Register 3.7. GDMA_OUT_INT_ENA_CHn_REG (n: 0-2) (0x0038+0x10*n)

| Bit 31 | ... | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|---|---|
|        |     | GDMA_OUTFIFO_OVF_CHn_INT_ENA | GDMA_OUTFIFO_UDF_CHn_INT_ENA | GDMA_OUT_TOTAL_EOF_CHn_INT_ENA | GDMA_OUT_DSCR_ERR_CHn_INT_ENA | GDMA_OUT_EOF_CHn_INT_ENA | GDMA_OUT_DONE_CHn_INT_ENA | Reset |

- **GDMA_OUT_DONE_CHn_INT_ENA** Write 1 to enable GDMA_OUT_DONE_CHn_INT. (R/W)
- **GDMA_OUT_EOF_CHn_INT_ENA** Write 1 to enable GDMA_OUT_EOF_CHn_INT. (R/W)
- **GDMA_OUT_DSCR_ERR_CHn_INT_ENA** Write 1 to enable GDMA_OUT_DSCR_ERR_CHn_INT. (R/W)
- **GDMA_OUT_TOTAL_EOF_CHn_INT_ENA** Write 1 to enable GDMA_OUT_TOTAL_EOF_CHn_INT. (R/W)
- **GDMA_OUTFIFO_OVF_CHn_INT_ENA** Write 1 to enable GDMA_OUTFIFO_OVF_CHn_INT. (R/W)
- **GDMA_OUTFIFO_UDF_CHn_INT_ENA** Write 1 to enable GDMA_OUTFIFO_UDF_CHn_INT. (R/W)

## Register 3.8. GDMA_OUT_INT_CLR_CHn_REG (n: 0-2) (0x003C+0x10*n)

| Bit 31 | ... | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|---|---|
|        |     | GDMA_OUTFIFO_OVF_CHn_INT_CLR | GDMA_OUTFIFO_UDF_CHn_INT_CLR | GDMA_OUT_TOTAL_EOF_CHn_INT_CLR | GDMA_OUT_DSCR_ERR_CHn_INT_CLR | GDMA_OUT_EOF_CHn_INT_CLR | GDMA_OUT_DONE_CHn_INT_CLR | Reset |

- **GDMA_OUT_DONE_CHn_INT_CLR** Write 1 to clear GDMA_OUT_DONE_CHn_INT. (WT)
- **GDMA_OUT_EOF_CHn_INT_CLR** Write 1 to clear GDMA_OUT_EOF_CHn_INT. (WT)
- **GDMA_OUT_DSCR_ERR_CHn_INT_CLR** Write 1 to clear GDMA_OUT_DSCR_ERR_CHn_INT. (WT)
- **GDMA_OUT_TOTAL_EOF_CHn_INT_CLR** Write 1 to clear GDMA_OUT_TOTAL_EOF_CHn_INT. (WT)
- **GDMA_OUTFIFO_OVF_CHn_INT_CLR** Write 1 to clear GDMA_OUTFIFO_OVF_CHn_INT. (WT)
- **GDMA_OUTFIFO_UDF_CHn_INT_CLR** Write 1 to clear GDMA_OUTFIFO_UDF_CHn_INT. (WT)
```