**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.213 EE.WR MASK_GPIO_OUT

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `011100100` ax[3:0] as[3:0] 0100

- **Assembler Syntax:**
  ```
  EE.WR_MASK_GPIO_OUT as, ax
  ```

- **Description:**
  It is a dedicated CPU GPIO instruction to set specified bits in GPIO_OUT. The lower 8 bits in register `ax` store the mask, and the lower 8 bits in register `as` store the assignment content.

- **Operation:**
  ```
  GPIO_OUT[7:0] = (GPIO_OUT[7:0] & ~ax[7:0]) | (as[7:0] & ax[7:0])
  ```

**Footer Information:**
- Page number and document version:
  - "296 ESP32-S3 TRM (Version 1.7)"
  
- Company information:
  - Espressif Systems

- Link for feedback or documentation submission:
  - Submit Documentation Feedback