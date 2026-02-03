**Title: Chapter 3 GDMA Controller (GDMA)**

---

**Register 3.18. GDMA_OUT_INT_CLR_CHn_REG (n: 0-4) (0x0074+192*n)**

| 31 | reserved |
|----|-----------|
| 0  |           |
| ... |           |
| 4  |           |

**Description:**  
GDMA_OUT_DONE_CHn_INT_CLR  
Set this bit to clear the GDMA_OUT_DONE_CH_INT interrupt. (WT)

---

**Register 3.18. GDMA_OUT_EOF_CHn_INT_CLR**

| 31 | reserved |
|----|-----------|
| 0  |           |
| ... |           |
| 4  |           |

**Description:**  
GDMA_OUT_EOF_CHn_INT_CLR  
Set this bit to clear the GDMA_OUT_EOF_CH_INT interrupt. (WT)

---

**Register 3.18. GDMA_OUT_DSCR_ERR_CHn_INT_CLR**

| 31 | reserved |
|----|-----------|
| 0  |           |
| ... |           |
| 4  |           |

**Description:**  
GDMA_OUT_DSCR_ERR_CHn_INT_CLR  
Set this bit to clear the GDMA_OUT_DSCR_ERR_CH_INT interrupt. (WT)

---

**Register 3.19. GDMA_EXTMEM_REJECT_INT_RAW_REG (0x03FC)**

| 31 | reserved |
|----|-----------|
| ... |           |

**Description:**  
GDMA_EXTMEM_REJECT_INT_RAW  
The raw interrupt bit turns to high level when accessing external RAM is rejected by permission control. (R/WTC/SS)

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

Page 388 ESP32-S3 TRM (Version 1.7)