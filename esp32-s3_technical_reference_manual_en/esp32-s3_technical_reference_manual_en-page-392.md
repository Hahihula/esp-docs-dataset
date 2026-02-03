**Title: Chapter 3 GDMA Controller (GDMA)**

---

**Section Title: Register 3.28. GDMA_IN_DSCR_BFO_CHn_REG**

- **Description:** 
  - `GDMA_INLLink_DSCR_BFO_CH0` represents the address of the current receive descriptor x that is pre-read.
  
- **Register Information:**
  - `GDMA_IN_DSCR_BFO_CHn_REG (n: 0-4) (0x0034+192*n)`
  - **Value:** 
    ```
    31       0
    ```

**Section Title: Register 3.29. GDMA_IN_DSCR_BF1_CHn_REG**

- **Description:**
  - `GDMA_INLLink_DSCR_BFO_CH0` represents the address of the previous receive descriptor x-1 that is pre-read.

- **Register Information:**
  - `GDMA_IN_DSCR_BF1_CHn_REG (n: 0-4) (0x0038+192*n)`
  - **Value:** 
    ```
    31       0
    ```

---

**Footer:**
- "Espressif Systems"
- Page number and document version:
  - `392`
  - "ESP32-S3 TRM (Version 1.7)"
  
- Link for submitting documentation feedback.
  - "Submit Documentation Feedback"