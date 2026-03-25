

```markdown
## 3.8 Registers

The addresses in this section are relative to GDMA base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 3.1. GDMA_IN_INT_RAW_Ch_n_REG (n: 0-2) (0x0000+0x10*n)

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 7   | GDMA_INFIFO_UDF_CHn_INT_RAW |
| 6   | GDMA_INFIFO_OVF_CHn_INT_RAW |
| 5   | GDMA_IN_DSCR_ERR_EOF_CHn_INT_RAW |
| 4   | GDMA_IN_DSCR_ERR_CHn_INT_RAW |
| 3   | GDMA_IN_DSCR_EMPTY_CHn_INT_RAW |
| 2   | GDMA_IN_SUC_EOF_CHn_INT_RAW |
| 1   | GDMA_IN_ERR_EOF_CHn_INT_RAW |
| 0   | GDMA_IN_DONE_CHn_INT_RAW |

GDMA_IN_DONE_Ch_n_INT_RAW The raw interrupt status of GDMA_IN_DONE_Ch_n_INT. (R/WTC/SS)

GDMA_IN_SUC_EOF_Ch_n_INT_RAW The raw interrupt status of GDMA_IN_SUC_EOF_Ch_n_INT. For UHCI this bit turns to 1 when the last data byte pointed by one receive descriptor has been received and no data error is detected for RX channel 0. (R/WTC/SS)

GDMA_IN_ERR_EOF_Ch_n_INT_RAW The raw interrupt status of GDMA_IN_ERR_EOF_Ch_n_INT. Valid only for UHCI or PARLIO. (R/WTC/SS)

GDMA_IN_DSCR_ERR_Ch_n_INT_RAW The raw interrupt status of GDMA_IN_DSCR_ERR_Ch_n_INT. (R/WTC/SS)

GDMA_IN_DSCR_EMPTY_Ch_n_INT_RAW The raw interrupt status of GDMA_IN_DSCR_EMPTY_Ch_n_INT. (R/WTC/SS)

GDMA_INFIFO_OVF_Ch_n_INT_RAW The raw interrupt status of GDMA_INFIFO_OVF_Ch_n_INT. (R/WTC/SS)

GDMA_INFIFO_UDF_Ch_n_INT_RAW The raw interrupt status of GDMA_INFIFO_UDF_Ch_n_INT. (R/WTC/SS)
```