**Title: Chapter 12 Timer Group (TIMG)**

---

### Register 12.7. TIMG_TxLOADLO_REG (\( x \): 0-1) (0x0018+0x24\*\( x \))

| Address | Value |
|---------|-------|
| **31**  | 0     |

TIMG_Tx_LOAD_LO  
Low 32 bits of the value that a reload will load onto timer \( x \) time-base counter. (R/W)

---

### Register 12.8. TIMG_TxLOADHI_REG (\( x \): 0-1) (0x001C+0x24\*\( x \))

| Address | Value |
|---------|-------|
| **31**  | 0     |

TIMG_Tx_LOAD_HI  
High 22 bits of the value that a reload will load onto timer \( x \) time-base counter. (R/W)

---

### Register 12.9. TIMG_TxLOAD_REG (\( x \): 0-1) (0x0020+0x24\*\( x \))

| Address | Value |
|---------|-------|
| **31**  | 0     |

TIMG_Tx_LOAD  
Write any value to trigger timer \( x \) time-base counter reload. (WT)

---

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

GoBack