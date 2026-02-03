**Chapter Title:**
Chapter 5 eFuse Controller

**GoBack Link:** GoBack

---

**Section Header (Register):**
Register 5.111. EFUSE_INT_RAW_REG (0x01D8)

**Binary Representation and Labels for Register 5.111:**
- Binary bits representation with labels:
  - EFUSE_READ_DONE_INT_RAW
  - EFUSE_PGM_DONE_INT_RAW

**Description of Register 5.111:**
EFUSE_READDone_INT_RAW The raw interrupt status of READ_DONE (R/WC/SS)
EFUSE_PGM_Done_INT_RAW The raw interrupt status of PGM_DONE (R/WC/SS)

---

**Section Header (Register):**
Register 5.112. EFUSE_INT_ST_REG (0x01DC)

**Binary Representation and Labels for Register 5.112:**
- Binary bits representation with labels:
  - EFUSE_READDone_INT_ST
  - EFUSE_PGM_Done_INT_ST

**Description of Register 5.112:**
EFUSE_READ_DONE_INT_ST The masked interrupt status of READ_DONE (RO)
EFUSE_PGM_DONE_INT_ST The masked interrupt status of PGM_DONE (RO)

---

**Section Header (Register):**
Register 5.113. EFUSE_INT_ENA_REG (0x01E0)

**Binary Representation and Labels for Register 5.113:**
- Binary bits representation with labels:
  - EFUSE_READDone_INT_ENA
  - EFUSE_PGM_Done_INT_ENA

**Description of Register 5.113:**
EFUSE_READ_DONE_INT_ENA Write 1 to enable READ_DONE (R/W)
EFUSE_PGM_DONE_INT_ENA Write 1 to enable PGM_DONE (R/W)

---

**Footer Information:** 
Espressif Systems
469 ESP32-S3 TRM (Version 1.7) 

**Link:**
Submit Documentation Feedback