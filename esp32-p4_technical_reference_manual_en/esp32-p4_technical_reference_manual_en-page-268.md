

```markdown
## Register 4.8. AHB_DMA_OUT_INT_CLR_CHn_REG (n: 0-2) (0x003C+0x10*n)

| Bit 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| (reserved) |    |    |    |    |    |    |    |    |    |    |    | AHB_DMA_OUT_RESP_ERR_CHn_INT_CLR | AHB_DMA_OUT_DSCR_ERR_CHn_INT_CLR | AHB_DMA_OUT_DONE_CHn_INT_CLR | AHB_DMA_OUT_EOF_CHn_INT_CLR | AHB_DMA_OUT_TOTAL_EOF_CHn_INT_CLR | AHB_DMA_OUTFIFO_OVF_CHn_INT_CLR | AHB_DMA_OUTFIFO_UDF_CHn_INT_CLR |    |    |    |    |    | Reset |

- `AHB_DMA_OUT_DONE_CHn_INT_CLR` Write 1 to clear AHB_DMA_OUT_DONE_CHn_INT. (WT)
- `AHB_DMA_OUT_EOF_CHn_INT_CLR` Write 1 to clear AHB_DMA_OUT_EOF_CHn_INT. (WT)
- `AHB_DMA_OUT_DSCR_ERR_CHn_INT_CLR` Write 1 to clear AHB_DMA_OUT_DSCR_ERR_CHn_INT. (WT)
- `AHB_DMA_OUT_TOTAL_EOF_CHn_INT_CLR` Write 1 to clear AHB_DMA_OUT_TOTAL_EOF_CHn_INT. (WT)
- `AHB_DMA_OUTFIFO_OVF_CHn_INT_CLR` Write 1 to clear AHB_DMA_OUTFIFO_OVF_CHn_INT. (WT)
- `AHB_DMA_OUTFIFO_UDF_CHn_INT_CLR` Write 1 to clear AHB_DMA_OUTFIFO_UDF_CHn_INT. (WT)
- `AHB_DMA_OUT_RESP_ERR_CHn_INT_CLR` Write 1 to clear AHB_DMA_OUT_RESP_ERR_CHn_INT. (WT)

## Register 4.9. AHB_DMA_AHB_TEST_REG (0x006C)

| Bit 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| (reserved) |    | AHB_DMA_AHB_TESTADDR | AHB_DMA_AHB_TESTMODE | (reserved) | Reset |

- `AHB_DMA_AHB_TESTMODE` Reserved. (R/W)
- `AHB_DMA_AHB_TESTADDR` Reserved. (R/W)
```