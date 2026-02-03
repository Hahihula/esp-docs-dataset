**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.157 EE.VMULAS.S8.QACC.LDBC.INCP.QUP

**Subsection Headers and Content:**

- **Instruction Word:** 
  - The instruction word is displayed in hexadecimal format.

- **Assembler Syntax:**
  - `EE.VMULAS.S8.QACC.LDBC.INCP.QUP qu, as, qx, qy, qs0, qs1`

- **Description:**
  - This section explains the operation of the instruction. It divides registers qx and qy into 16 data segments by 8 bits.
  - The signed multiplication result is added to a corresponding special register (QACC_H or QACC_L).
  - The calculated value is saturated, stored in the specified segment as an unsigned number.

- **Operation:**
  - Detailed operation steps are provided with hexadecimal values and operations. For example:
    ```
    QACC_L[19:0] = min(max(QACC_L[19:0] + qx[7:0], 7) * qy[7:0], -2^{19}), 2^{19}-1)
    ```

**Footer Information:** 
- "Espressif Systems"
- Page number and document version information:
  - ESP32-S3 TRM (Version 1.7)

**Navigation Link:**
- GoBack

**Feedback Option:**
- Submit Documentation Feedback