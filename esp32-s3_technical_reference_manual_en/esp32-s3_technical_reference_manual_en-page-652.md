**Title:**
Chapter 11 System Timer (SYSTIMER)

**Subtitles and Body Text with Descriptions of Registers:**

- **Register 11.31. SYSTIMER_REAL_TARGETO_HI_REG (0x0078)**
  - Description:
    - `SYSTIMER TARGETO_HI_RO`
    - Actual target value of COMPO, high 20 bits.
    - (RO)
  - Binary representation: 
    ```
    31  20  19
    0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    ```

- **Register 11.32. SYSTIMER_REAL_TARGET1_LO_REG (0x007C)**
  - Description:
    - `SYSTIMER TARGETI_LO_RO`
    - Actual target value of COMP1, low 32 bits.
    - (RO)
  - Binary representation: 
    ```
    31   0
    ```

- **Register 11.33. SYSTIMER_REAL_TARGET1_HI_REG (0x0080)**
  - Description:
    - `SYSTIMER TARGETI_HI_RO`
    - Actual target value of COMP1, high 20 bits.
    - (RO)
  - Binary representation: 
    ```
    31   20  19
    0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
    ```

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)