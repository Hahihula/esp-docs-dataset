**Title:**
Chapter 11 System Timer (SYSTIMER)

**Subtitles and Content with Structure Indications:**

- **Register 11.28. SYSTIMER_INT_CLR_REG (0x006C)**
  - **Binary Representation:** 
    ```
    3 | 2 | 1 | 0
    -------------------
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```
  - **Description:**
    - SYSTIMER_TARGETO_INT_CLR: SYSTIMER_TARGETO_INT clear bit. (WT)
    - SYSTIMER_TARGET1_INT_CLR: SYSTIMER_TARGET1_INT clear bit. (WT)
    - SYSTIMER_TARGET2_INT_CLR: SYSTIMER_TARGET2_INT clear bit. (WT)

- **Register 11.29. SYSTIMER_INT_ST_REG (0x0070)**
  - **Binary Representation:** 
    ```
    3 | 2 | 1 | 0
    -------------------
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```
  - **Description:**
    - SYSTIMER_TARGETO_INT_ST: SYSTIMER_TARGETO_INT status bit. (RO)
    - SYSTIMER_TARGET1_INT_ST: SYSTIMER_TARGET1_INT status bit. (RO)
    - SYSTIMER_TARGET2_INT_ST: SYSTIMER_TARGET2_INT status bit. (RO)

- **Register 11.30. SYSTIMER_REAL TARGETO_LO_REG (0x0074)**
  - **Binary Representation:** 
    ```
    3 | 2 | 1 | 0
    -------------------
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```
  - **Description:**
    - SYSTIMER_TARGETO_LO_RO: Actual target value of COMPO, low 32 bits. (RO)

**Footer Information:**
- Page number and document version:
  - "651 ESP32-S3 TRM (Version 1.7)"
- Company information:
  - Espressif Systems
- Feedback link:
  - Submit Documentation Feedback

**Navigation Link:**
- GoBack