**Title:**
Chapter 15 Permission Control (PMS)

**Subtitle:**
Register 15.71. PMS_EDMA_BOUNDARY_2_REG (0x02B4)

**Body Text and Diagrams with Descriptions:**

- **Diagram Description:** 
  - A register diagram labeled "PMS_EDMABOUNDARY_2" showing a bit pattern.
  - Bits are numbered from left to right, starting at the most significant bit on the far left (bit position is indicated as '31' for MSB and '0' for LSB).
  - The bits in between have labels such as "reserved".
  - There's an arrow pointing towards a specific set of bits labeled "Reset" with value `0x2000`.

- **Text Description:**
  - PMS_EDMABOUNDARY_2 Configures the ending address of external SRAM area. For details, see Table 15.5-3.
  - (R/W)

**Subtitle:**
Register 15.72. PMS_EDMA_PMS_SPI2_LOCK_REG (0x02B8)

**Body Text and Diagrams with Descriptions:**

- **Diagram Description:** 
  - Another register diagram labeled "PMS_EDMAPMS_SPI2_LOCK" showing a bit pattern.
  - Bits are numbered from left to right, starting at the most significant bit on the far left (bit position is indicated as '31' for MSB and '0' for LSB).
  - The bits in between have labels such as "reserved".
  - There's an arrow pointing towards a specific set of bits labeled "Reset" with value `0`.

- **Text Description:**
  - PMS_EDMA_PMS_SPI2_LOCK Set this bit to lock the register that configures SPI2’s access to external SRAM.
  - (R/W)

**Footer Information:** 
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback
- GoBack

(Note: The text "Submit Documentation Feedback" and "GoBack" appear as part of the footer or navigation elements, not directly related to technical content.)