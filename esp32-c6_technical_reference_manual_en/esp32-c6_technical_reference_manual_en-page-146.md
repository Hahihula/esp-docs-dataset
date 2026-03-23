

```markdown
Register 4.2: GDMA_IN_INT_ST_CHn_REG (n: 0-2) (0x0004+0x10*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | Reset                                                                       |
| 7   | GDMA_INFIFO_UFCHO_INT_ST                                                   |
| 6   | GDMA_IN_INFIFO_OVF_INT_ST                                                  |
| 5   | GDMA_IN_DSCR_ERR_CHn_INT_ST                                                |
| 4   | GDMA_IN_SUC_EOF_CHn_INT_ST                                                 |
| 3   | GDMA_IN_ERR_EOF_CHn_INT_ST                                                 |
| 2   | GDMA_IN_DONE_CHn_INT_ST                                                     |
| 1   | GDMA_IN_DSCR_EMPTY_CHn_INT_ST                                               |
| 0   | (reserved)                                                                  |

GDMA_IN_DONE_CHn_INT_ST The masked interrupt status of GDMA_IN_DONE_CHn_INT. (RO)

GDMA_IN_SUC_EOF_CHn_INT_ST The masked interrupt status of GDMA_IN_SUC_EOF_CHn_INT. (RO)

GDMA_IN_ERR_EOF_CHn_INT_ST The masked interrupt status of GDMA_IN_ERR_EOF_CHn_INT. (RO)

GDMA_IN_DSCR_ERR_CHn_INT_ST The masked interrupt status of GDMA_IN_DSCR_ERR_CHn_INT. (RO)

GDMA_IN_DSCR_EMPTY_CHn_INT_ST The masked interrupt status of GDMA_IN_DSCR_EMPTY_CHn_INT. (RO)

GDMA_INFIFO_OVF_CHn_INT_ST The masked interrupt status of GDMA_INFIFO_OVF_CHn_INT. (RO)

GDMA_INFIFO_UFCHn_INT_ST The masked interrupt status of GDMA_INFIFO_UFCHn_INT. (RO)
```