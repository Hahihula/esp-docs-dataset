

```markdown
Register 3.6. GDMA_OUT_INT_ST_CHn_REG (n: 0-2) (0x0034+0x10*n)

| Bit 31 | ... | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|---|---|
|        | (reserved) | GDMA_OUTFIFO_UDF_CHn_INT_ST | GDMA_OUTFIFO_OVF_CHn_INT_ST | GDMA_OUT_DSCR_ERR_CHn_INT_ST | GDMA_OUT_TOTAL_EOF_CHn_INT_ST | GDMA_OUT_DONE_CHn_INT_ST |
| Reset  |         |                         |                          |                               |                              |

GDMA_OUT_DONE_CHn_INT_ST    The masked interrupt status of GDMA_OUT_DONE_CHn_INT. (RO)

GDMA_OUT_EOF_CHn_INT_ST     The masked interrupt status of GDMA_OUT_EOF_CHn_INT. (RO)

GDMA_OUT_DSCR_ERR_CHn_INT_ST The masked interrupt status of GDMA_OUT_DSCR_ERR_CHn_INT. (RO)

GDMA_OUT_TOTAL_EOF_CHn_INT_ST The masked interrupt status of GDMA_OUT_TOTAL_EOF_CHn_INT. (RO)

GDMA_OUTFIFO_OVF_CHn_INT_ST  The masked interrupt status of GDMA_OUTFIFO_OVF_CHn_INT. (RO)

GDMA_OUTFIFO_UDF_CHn_INT_ST  The masked interrupt status of GDMA_OUTFIFO_UDF_CHn_INT. (RO)
```