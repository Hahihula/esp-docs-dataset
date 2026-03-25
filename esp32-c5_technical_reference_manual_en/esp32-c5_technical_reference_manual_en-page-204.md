

```markdown
## 5.9 Registers

The addresses in this section are relative to GDMA base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 5.1. AHB_DMA_IN_INT_RAW_CHn_REG (n: 0-2) (0x0000+0x10*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | Reset                                                                       |
| 8   | AHIB_DMA_IN_DONE_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_DONE_CHn_INT. (R/WTC/SS) |
|     | AHIB_DMA_IN_SUC_EOF_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_SUC_EOF_CHn_INT. For UHCI, this bit turns to 1 when the last data byte pointed by one receive descriptor has been received and no data error is detected for RX channel n. (R/WTC/SS) |
|     | AHIB_DMA_IN_ERR_EOF_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_ERR_EOF_CHn_INT. Valid only for UHCI. (R/WTC/SS) |
|     | AHIB_DMA_IN_DSCR_ERR_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_DSCR_ERR_CHn_INT. (R/WTC/SS) |
|     | AHIB_DMA_IN_DSCR_EMPTY_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_DSCR_EMPTY_CHn_INT. (R/WTC/SS) |
|     | AHIB_DMA_INFIFO_OVF_CHn_INT_RAW The raw interrupt status of AHB_DMA_INFIFO_OVF_CHn_INT. (R/WTC/SS) |
|     | AHIB_DMA_INFIFO_UDF_CHn_INT_RAW The raw interrupt status of AHB_DMA_INFIFO_UDF_CHn_INT. (R/WTC/SS) |
|     | AHIB_DMA_IN_RESP_ERR_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_RESP_ERR_CHn_INT. (R/WTC/SS) |
```