

```markdown
Register 4.4. GDMA_IN_INT_CLR_CHn_REG (n: 0-2) (0x000C+0x10*n)

31      7 6 5 4 3 2 1 0
+------+------+------+------+------+------+------+
| (reserved) | GDMA_INFIFO_UDF_CHO_INT_CLR | GDMA_INFIFO_OVF_CHO_INT_CLR | GDMA_IN_DSCR_ERR_CHO_INT_CLR | GDMA_IN_DSCR_EMPTY_CHO_INT_CLR | GDMA_IN_SUC_EOF_CHO_INT_CLR | GDMA_IN_DONE_CHO_INT_CLR |
+------+------+------+------+------+------+------+
Reset

GDMA_IN_DONE_CHn_INT_CLR   Write 1 to clear GDMA_IN_DONE_CHn_INT. (WT)
GDMA_IN_SUC_EOF_CHn_INT_CLR Write 1 to clear GDMA_IN_SUC_EOF_CHn_INT. (WT)
GDMA_IN_ERR_EOF_CHn_INT_CLR Write 1 to clear GDMA_IN_ERR_EOF_CHn_INT. (WT)
GDMA_IN_DSCR_ERR_CHn_INT_CLR Write 1 to clear GDMA_IN_DSCR_ERR_CHn_INT. (WT)
GDMA_IN_DSCR_EMPTY_CHn_INT_CLR Write 1 to clear GDMA_IN_DSCR_EMPTY_CHn_INT. (WT)
GDMA_INFIFO_OVF_CHn_INT_CLR Write 1 to clear GDMA_INFIFO_OVF_CHn_INT. (WT)
GDMA_INFIFO_UDF_CHn_INT_CLR Write 1 to clear GDMA_INFIFO_UDF_CHn_INT. (WT)
```