**Chapter Title:**
Chapter 38 Pulse Count Controller (PCNT)

**GoBack Link:** GoBack

---

**Register Information and Description**

- **Register Name**: PCNT_INT_RAW_REG (0x0040)
  - **Description**: 
    ```
    PCNT_CNT THR EVENT U_n INT RAW
    The raw interrupt status bit for the
    PCNT_CNT THR EVENT Un INT interrupt. (RO)
    ```
  - **Bit Description**:
    ```
    31 reserved
    4 to 0 Reset
    ```

- **Register Name**: PCNT_INT_ST_REG (0x0044)
  - **Description**:
    ```
    PCNT_CNT THR EVENT U_n INT ST
    The masked interrupt status bit for the
    PCNT_CNT THR EVENT Un INT interrupt. (RO)
    ```
  - **Bit Description**:
    ```
    31 reserved
    4 to 0 Reset
    ```

- **Register Name**: PCNT_INT_ENA_REG (0x0048)
  - **Description**:
    ```
    PCNT_CNT THR EVENT U_n INT ENA
    The interrupt enable bit for the
    PCNT_CNT THR EVENT Un INT interrupt. (R/W)
    ```
  - **Bit Description**:
    ```
    31 reserved
    4 to 0 Reset
    ```

---

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 1451

**Action Links:** Submit Documentation Feedback