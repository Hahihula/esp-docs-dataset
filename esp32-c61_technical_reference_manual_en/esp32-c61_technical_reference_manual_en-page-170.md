

```markdown
## 3.9 Registers

The addresses in this section are relative to GDMA base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 3.1. AHB_DMA_IN_INT_RAW_CHn_REG (n: 0-1) (0x0000+0x10*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | Reset                                                                       |
| ... |                                                                             |
| 7   | AHB_DMA_INFIFO_UF_CHn_INT_RAW                                               |
| 6   | AHB_DMA_INFIFO_OVF_CHn_INT_RAW                                              |
| 5   | AHB_DMA_IN_DSCR_ERR_CHn_INT_RAW                                             |
| 4   | AHB_DMA_IN_DSCR_EMPTY_CHn_INT_RAW                                           |
| 3   | AHB_DMA_IN_SUC_EOF_CHn_INT_RAW                                              |
| 2   | AHB_DMA_IN_DONE_CHn_INT_RAW                                                |

AHB_DMA_IN_DONE_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_DONE_CHn_INT. (R/WTC/SS)

AHB_DMA_IN_SUC_EOF_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_SUC_EOF_CHn_INT. (R/WTC/SS)

AHB_DMA_IN_DSCR_ERR_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_DSCR_ERR_CHn_INT. (R/WTC/SS)

AHB_DMA_IN_DSCR_EMPTY_CHn_INT_RAW The raw interrupt status of AHB_DMA_IN_DSCR_EMPTY_CHn_INT. (R/WTC/SS)

AHB_DMA_INFIFO_OVF_CHn_INT_RAW The raw interrupt status of AHB_DMA_INFIFO_OVF_CHn_INT. (R/WTC/SS)

AHB_DMA_INFIFO_UF_CHn_INT_RAW The raw interrupt status of AHB_DMA_INFIFO_UF_CHn_INT. (R/WTC/SS)
```