**Title:**
Chapter 20 SPI Controller (SPI)

**Header:**
GoBack

**Register Information:**
- Register Name: SPI_RD_STATUS_REG (0x10)
- Description of the register contents:
  - **SPI_STATUS_EXT**: Reserved.
    - Binary representation with bits labeled from right to left as follows:
      ```
      31 | 24 | 23 | 16 | 15
      SPI_STATUS_EXT
      ```
      Values: `0x000`
  - **SPI_STATUS**: Reserved.

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type:
  - Page Number: "368"
  - Document Title: ESP32 TRM (Version 5.6)
- Link Texts:
  - Submit Documentation Feedback

The image also contains a diagram with binary bit labels from right to left, showing the layout of bits in registers SPI_STATUS_EXT and SPI_STATUS within register SPI_RD_STATUS_REG.

**Reset Indicator:**
- The word "Reset" is placed next to one column under the binary representation.