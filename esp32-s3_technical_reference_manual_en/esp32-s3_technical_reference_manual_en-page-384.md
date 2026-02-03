**Title:**
Chapter 3 GDMA Controller (GDMA)

**Subtitle:**
Register 3.13. GDMA_IN_INT_ENA_CHn_REG (n: 0-4) (0x0010+192*n)

**Body Text with Table:**

| Address | Name                          |
|---------|-------------------------------|
| 0       | GDMA_IN_DONE_CHn_INT_ENA     |
|        | The interrupt enable bit for the GDMA_INDone_CH_INT interrupt. (R/W) |
| 4       | GDMA_IN_SUC_EOF_CHn_INT_ENA  |
|        | The interrupt enable bit for the GDMA_INSuc_EOF_CH_INT interrupt. (R/W) |
| 8       | GDMA_IN_ERR_EOF_CHn_INT_ENA  |
|        | The interrupt enable bit for the GDMA_INErr_EOF_CH_INT interrupt. (R/W) |
| 12      | GDMA_IN_DSCR_ERR_CHn_INT_ENA |
|        | The interrupt enable bit for the GDMA_INDSCR_Err_CH_INT interrupt. (R/W) |
| 16      | GDMA_IN_DSCR_EMPTY_CHn_INT_ENA |
|        | The interrupt enable bit for the GDMA_INDSCR_Empty_CH_INT interrupt. (R/W) |
| 20      | GDMA_INFIFO_FULL_WM_CHn_INT_ENA |
|        | The interrupt enable bit for the GDMA_INFIFOFull_WM_CH_INT interrupt. (R/W) |

**Footer:**
Espressif Systems
384 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback