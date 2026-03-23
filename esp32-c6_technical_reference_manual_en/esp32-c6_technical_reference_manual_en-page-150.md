

```markdown
Register 4.6. GDMA_OUT_INT_ST_CHn_REG (n: 0-2) (0x0034+0x10*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  |                                             |                                                                             |
| 29  |                                             |                                                                             |
| ... | ...                                       | ...                                                                         |
| 6   | GDMA_OUTFIFO_UDF_CHn_INT_ST                | The masked interrupt status of GDMA_OUTFIFO_UDF_CHn_INT. (RO)               |
| 5   | GDMA_OUTFIFO_OVF_CHn_INT_ST                | The masked interrupt status of GDMA_OUTFIFO_OVF_CHn_INT. (RO)               |
| 4   | GDMA_OUT_TOTAL_EOF_CHn_INT_ST              | The masked interrupt status of GDMA_OUT_TOTAL_EOF_CHn_INT. (RO)             |
| 3   | GDMA_OUT_DSCR_ERR_CHn_INT_ST               | The masked interrupt status of GDMA_OUT_DSCR_ERR_CHn_INT. (RO)              |
| 2   |                                             |                                                                             |
| 1   |                                             |                                                                             |
| 0   | Reset                                      |                                                                             |

GDMA_OUT_DONE_CHn_INT_ST    The masked interrupt status of GDMA_OUT_DONE_CHn_INT. (RO)

GDMA_OUT_EOF_CHn_INT_ST     The masked interrupt status of GDMA_OUT_EOF_CHn_INT. (RO)

GDMA_OUT_DSCR_ERR_CHn_INT_ST The masked interrupt status of GDMA_OUT_DSCR_ERR_CHn_INT. (RO)

GDMA_OUT_TOTAL_EOF_CHn_INT_ST The masked interrupt status of GDMA_OUT_TOTAL_EOF_CHn_INT. (RO)

GDMA_OUTFIFO_OVF_CHn_INT_ST  The masked interrupt status of GDMA_OUTFIFO_OVF_CHn_INT. (RO)

GDMA_OUTFIFO_UDF_CHn_INT_ST  The masked interrupt status of GDMA_OUTFIFO_UDF_CHn_INT. (RO)
```