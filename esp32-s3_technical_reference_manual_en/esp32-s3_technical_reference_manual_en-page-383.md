**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Section Header:**
Register 3.12. GDMA_IN_INT_ST_CHn_REG (n: 0-4) (0x000C+192*n)

**Binary Representation Table:**
```
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
```

**Text and Descriptions:**
- GDMA_IN_DONE_CHn_INT_ST The raw interrupt status bit for the GDMA_IN_DONE_CH_n interrupt. (RO)
- GDMA_IN_SUC_EOF_CHn_INT_ST The raw interrupt status bit for the GDMA_IN_SUC_EOF_CH_n interrupt. (RO)
- GDMA_IN_ERR_EOF_CHn_INT_ST The raw interrupt status bit for the GDMA_IN_ERR_EOF_CH_n interrupt. (RO)
- GDMA_IN_DSCR_ERR_CHn_INT ST The raw interrupt status bit for the GDMA_IN_DSCR_ERR_CH_n interrupt. (RO)
- GDMA_IN_DSCR_EMPTY_CHn_INT ST The raw interrupt status bit for the GDMA_IN_DSCR_EMPTY_CH_n interrupt. (RO)
- GDMA_IN_INFIFO_FULL_WM_CHn_INT_ST The raw interrupt status bit for the GDMA_IN_INFIFO_FULL_WM_CH_n interrupt. (RO)

**Footer:**
Espressif Systems
383 ESP32-S3 TRM (Version 1.7) Submit Documentation Feedback