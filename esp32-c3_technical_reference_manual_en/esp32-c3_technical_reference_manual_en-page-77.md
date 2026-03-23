

```markdown
Register 2.4. GDMA_INT_CLR_CHn_REG (n: 0-2) (0x00C+16*n)

31                                 13 12 11 10 9 8 7 6 5 4 3 2 1 0
+------------------------------------------------------------------+ Reset
| (reserved)                                                       |
| GDMA_OUTFIFO_UDF_CHn_INT_CLR | GDMA_INFIFO_OVF_CHn_INT_CLR | GDMA_IN_DSCR_ERR_CHn_INT_CLR | ... | GDMA_OUT_DONE_CHn_INT_CLR |

GDMA_IN_DONE_CHn_INT_CLR  Set this bit to clear the GDMA_IN_DONE_CH_INT interrupt. (WT)
GDMA_IN_SUC_EOF_CHn_INT_CLR  Set this bit to clear the GDMA_IN_SUC_EOF_CH_INT interrupt. (WT)
GDMA_IN_ERR_EOF_CHn_INT_CLR  Set this bit to clear the GDMA_IN_ERR_EOF_CH_INT interrupt. (WT)
GDMA_OUT_DONE_CHn_INT_CLR  Set this bit to clear the GDMA_OUT_DONE_CH_INT interrupt. (WT)
GDMA_OUT_EOF_CHn_INT_CLR  Set this bit to clear the GDMA_OUT_EOF_CH_INT interrupt. (WT)
GDMA_IN_DSCR_ERR_CHn_INT_CLR  Set this bit to clear the GDMA_IN_DSCR_ERR_CH_INT interrupt. (WT)
GDMA_OUT_DSCR_ERR_CHn_INT_CLR  Set this bit to clear the GDMA_OUT_DSCR_ERR_CH_INT interrupt. (WT)
GDMA_IN_DSCR_EMPTY_CHn_INT_CLR  Set this bit to clear the GDMA_IN_DSCR_EMPTY_CH_INT interrupt. (WT)
GDMA_OUT_TOTAL_EOF_CHn_INT_CLR  Set this bit to clear the GDMA_OUT_TOTAL_EOF_CH_INT interrupt. (WT)
GDMA_INFIFO_OVF_CHn_INT_CLR  Set this bit to clear the GDMA_INFIFO_OVF_L1_CH_INT interrupt. (WT)
GDMA_INFIFO_UDF_CHn_INT_CLR  Set this bit to clear the GDMA_INFIFO_UDF_L1_CH_INT interrupt. (WT)
GDMA_OUTFIFO_OVF_CHn_INT_CLR  Set this bit to clear the GDMA_OUTFIFO_OVF_L1_CH_INT interrupt. (WT)
GDMA_OUTFIFO_UDF_CHn_INT_CLR  Set this bit to clear the GDMA_OUTFIFO_UDF_L1_CH_INT interrupt. (WT)
```