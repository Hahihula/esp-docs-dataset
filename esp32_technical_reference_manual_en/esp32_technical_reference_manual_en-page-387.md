**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**GoBack Link:** GoBack

---

**Section Header and Description with Address Information for Each Register**

- **Register 20.40. SPI_OUTLINK_DSCR_REG (0x13C)**
  - Binary representation of the register address.
  - Description: The address of the current outlink descriptor.

- **Register 20.41. SPI_OUTLINK_DSCR_BFO_REG (0x140)**
  - Binary representation of the register address.
  - Description: The address of the next outlink descriptor.

- **Register 20.42. SPI_OUTLINK_DSCR_BF1_REG (0x144)**
  - Binary representation of the register address.
  - Description: The address of the next outlink data buffer.

- **Register 20.43. SPI_DMA_RSTATUS_REG (0x148)**
  - Binary representation of the register address and fields within it:
    - TX_FIFO_EMPTY
      - Description: The SPI DMA TX FIFO is empty.
    - TX_FIFO_FULL
      - Description: The SPI DMA TX FIFO is full.
    - TX_DESC_ADDRESS
      - Description: The LSB of the SPI DMA outlink descriptor address.

---

**Footer Information**
- Company Name: Espressif Systems
- Document Version and Type: ESP32 TRM (Version 5.6)
- Submit Documentation Feedback Link

(Note: Binary representations are shown as they appear in images, with '0' indicating a bit position.)