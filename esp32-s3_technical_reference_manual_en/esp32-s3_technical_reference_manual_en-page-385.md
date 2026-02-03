**Title:**
Chapter 3 GDMA Controller (GDMA)

**Register Information:**
- Register Name: GDMA_IN_INT_CLR_CHn_REG
- Offset Range: n = 0-4, Address Format: 0x0014+192*n

**Bit Description Table:**

| Bit Number | Bit Name                          |
|------------|-----------------------------------|
| 31         | (reserved)                        |
| ...        | ...                               |
| 6          | GDMA_DMA_INFO_FULL_WM             |
| 5          | GDMA_DMA_INFO_EMPTY_CH            |
| 4          | GDMA_DMA_ERR_EOF_INT_CLR          |
| 3          | GDMA_IN_DONE_CH_INT              |
| 2          | GDMA_IN_ERR_EOF_CH_INT           |
| 1          | GDMA_INDoneErrChIntCLR           |
| 0          | (reserved)                        |

**Description of Each Bit:**

- **GDMA_IN_DONE_CHn_INT_CLR**: Set this bit to clear the GDMA_IN_DONE_CH_INT interrupt. (WT)
- **GDMA_IN_SUC_EOF_CHn_INT_CLR**: Set this bit to clear the GDMA_IN_SUC_EOF_CH_INT interrupt.
- **GDMA_IN_ERR_EOF_CHn_INT_CLR**: Set this bit to clear the GDMA_IN_ERR_EOF_CH_INT interrupt.
- **GDMA_IN_DSCR_ERR_CHn_INT_CLR**: Set this bit to clear the GDMA_IN_DSCR_ERR_CH_INT interrupt. (WT)
- **GDMA_IN_DSCR_EMPTY_CHn_INT_CLR**: Set this bit to clear the GDMA_IN_DSCR_EMPTY_CH_INT interrupt.

**Additional Information:**

- **GDMA_DMA_INFIFO_FULL_WM_CHn_INT_CLR**: Set this bit to clear the GDMA_DMA_INFIFO_FULL_WM_CH_INT interrupt. (WT)

**Footer:**
Espressif Systems
Page Number: 385
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- Submit Documentation Feedback