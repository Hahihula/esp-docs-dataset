**Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Subtitles and Body Texts with Descriptions of Registers:**

- **Register 31.7, TWAI_DATA_2_REG (0x0048)**
  - **TWAI_TX_BYTE_2**: Stored the 2nd byte information of the data to be transmitted in operation mode.
    - Access Type: WO
  - **TWAI_ACCEPTANCE_CODE_2**: Stored the 2nd byte of the filter code in reset mode.
    - Access Type: R/W

- **Register 31.8, TWAI_DATA_3_REG (0x004C)**
  - **TWAI_TX_BYTE_3**: Stored the 3rd byte information of the data to be transmitted in operation mode.
    - Access Type: WO
  - **TWAI_ACCEPTANCE_CODE_3**: Stored the 3rd byte of the filter code in reset mode.
    - Access Type: R/W

**Footer Information:**
- Espressif Systems, Page Number (1217), Document Version (ESP32-S3 TRM, Version 1.7)
- Links for Submitting Documentation Feedback and GoBack to previous page.

**Diagrams/Tables Description in Markdown Format with Labels as Described on Image:**

- **TWAI_TX_BYTE_2 Diagram**: Shows a register layout where the bits are labeled from left (bit position) to right, starting at 31. The label "Reset" is placed next to bit positions.
  
- **TWAI_TX_BYTE_3 Diagram**: Similar structure as TWAI_TX_BYTE_2 with corresponding labels and reset indication.

**Note:**
The red text annotations on the diagrams are not part of standard documentation but seem like additional notes or highlights for specific bits.