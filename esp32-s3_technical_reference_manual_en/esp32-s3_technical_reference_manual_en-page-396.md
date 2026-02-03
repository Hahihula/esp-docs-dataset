**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Section Header:**
GoBack

**Register Information and Description:**

- **Register Name:** Register 3.36, GDMA_OUT_DSCR_BF1_CHn_REG (n: 0-4) (0x0098+192*n)
  
  - **Description:** Represents the address of the previous transmit descriptor y-1 that is pre-read.

- **Register Name:** Register 3.37, GDMA_INPRI_CHn_REG (n: 0-4) (0x0044+192*n)

  - **Description:** The priority of RX channel n.
  
    - **Bit Description:**
      ```
      31   0
      0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
      ```
  
- **Register Name:** Register 3.38, GDMA_OUTPRI_CHn_REG (n: 0-4) (0x00A4+192*n)

  - **Description:** The priority of TX channel n.
  
    - **Bit Description:**
      ```
      31   reserved
      4     0
      0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
      ```
  
**Footer:**
Espressif Systems

**Document Information:** 
ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
Submit Documentation Feedback