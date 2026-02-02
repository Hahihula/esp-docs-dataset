**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Section Titles and Descriptions with Registers Information:**

1. **Register Description:** 
   - **Title:** Register 23.4. PCNT_Un_CNT_REG (n; 0-7) (0x60+0x04*n)
   - **Description:** This register stores the current pulse count value for unit n.
   - **Bit Layout:**
     ```
     31    16    15
     0 0 0 0 0 0 0 0 0 x000000 Reset
     ```

2. **Register Description:** 
   - **Title:** Register 23.5. PCNT_INT_RAW_REG (0x0080)
   - **Description:** The raw interrupt status bit for the PCNT_CNT THR EVENT Un INT interrupt.
   - **Bit Layout:**
     ```
     31    8
     0x0000000 Reset
     ```

3. **Register Description:** 
   - **Title:** Register 23.6. PCNT_INT_ST_REG (0x0084)
   - **Description:** The masked interrupt status bit for the PCNT_CNT THR EVENT Un INT interrupt.
   - **Bit Layout:**
     ```
     31    8
     0x0000000 Reset
     ```

**Footer Information:**
- Page Number: 458
- Document Version: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Navigation Links:** 
- Submit Documentation Feedback