**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**GoBack Link:** GoBack

---

**Section Header: Register Information**

- **Register Name and Address:**
  - **Register 20.35. SPI_INLINK_DSCR_REG (0x128)**
    - Description:
      ```
      SPI_INLINK_DSCR_REG
      The address of the current inlink descriptor.
      (RO)
      ```
    - Hexadecimal representation with bits labeled: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`

- **Register Name and Address:**
  - **Register 20.36. SPI_INLINK_DSCR_BFO_REG (0x12C)**
    - Description:
      ```
      SPI_INLINK_DSCR_BFO_REG
      The address of the next inlink descriptor.
      (RO)
      ```
    - Hexadecimal representation with bits labeled: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`

- **Register Name and Address:**
  - **Register 20.37. SPI_INLINK_DSCR_BF1_REG (0x130)**
    - Description:
      ```
      SPI_INLINK_DSCR_BF1_REG
      The address of the next inlink data buffer.
      (RO)
      ```
    - Hexadecimal representation with bits labeled: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`

- **Register Name and Address:**
  - **Register 20.38. SPI_OUT_EOF_BFRDES_ADDR_REG (0x134)**
    - Description:
      ```
      SPI_OUT_EOF_BFRDES_ADDR_REG
      The buffer address corresponding to the outlink descriptor that produces EOF.
      (RO)
      ```
    - Hexadecimal representation with bits labeled: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`

- **Register Name and Address:**
  - **Register 20.39. SPI_OUT_EOF_DES_ADDR_REG (0x138)**
    - Description:
      ```
      SPI_OUT_EOF_DES_ADDR_REG
      The last outlink descriptor address when SPI DMA encountered EOF.
      (RO)
      ```
    - Hexadecimal representation with bits labeled: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`

---

**Footer Information:**  
Espressif Systems  
386 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback