

```markdown
Register 4.5. GDMA_OUT_INT_RAW_CHn_REG (n: 0-2) (0x0030+0x10*n)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 6   | GDMA_OUTFIFO_UDF_CHn_INT_RAW           | The raw interrupt status of GDMA_OUTFIFO_UDF_CHn_INT. (R/WTC/SS)             |
| 5   | GDMA_OUTFIFO_OVF_CHn_INT_RAW           | The raw interrupt status of GDMA_OUTFIFO_OVF_CHn_INT. (R/WTC/SS)             |
| 4   | GDMA_OUT_DONE_CHn_INT_RAW              | The raw interrupt status of GDMA_OUT_DONE_CHn_INT. (R/WTC/SS)                |
| 3   | GDMA_OUT_EOF_CHn_INT_RAW               | The raw interrupt status of GDMA_OUT_EOF_CHn_INT. (R/WTC/SS)                 |
| 2   | GDMA_OUT_DSCR_ERR_CHn_INT_RAW          | The raw interrupt status of GDMA_OUT_DSCR_ERR_CHn_INT. (R/WTC/SS)            |
| 1   | GDMA_OUT_TOTAL_EOF_CHn_INT_RAW         | The raw interrupt status of GDMA_OUT_TOTAL_EOF_CHn_INT. (R/WTC/SS)           |
```