**Title: Chapter 3 GDMA Controller (GDMA)**

---

### Register 3.33. GDMA_OUT_EOF_BFR_DESCR_ADDR_CHn_REG (n : 0-4) (0x008C+192*n)

| Field | Value |
|-------|-------|
| 31    | 0     |

**Description:**
GDMA_OUT_EOF_BFR_DESCR_ADDR_CHn  
This register stores the address of the transmit descriptor before the last transmit descriptor. (RO)

---

### Register 3.34. GDMA_OUT_DSCR_CHn_REG (n : 0-4) (0x0090+192*n)

| Field | Value |
|-------|-------|
| 31    | 0     |

**Description:**
GDMA_OUTLINK_DSCR_CHn  
Represents the address of the next transmit descriptor y+1 pointed by the current transmit descriptor that is pre-read. (RO)

---

### Register 3.35. GDMA_OUT_DSCR_BFO_CHn_REG (n : 0-4) (0x0094+192*n)

| Field | Value |
|-------|-------|
| 31    | 0     |

**Description:**
GDMA_OUTLINK_DSCR_BFO_CHn  
Represents the address of the current transmit descriptor y that is pre-read. (RO)

---

**Footer:** 
Espressif Systems  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)