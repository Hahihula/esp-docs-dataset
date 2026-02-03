**Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Subtitles and Body Texts with Descriptions of Registers:**

- **Register 31.5. TWAI_DATA_0_REG (0x0040)**
  - **TWAI_TX_BYTE_0**: Stored the Oth byte information of the data to be transmitted in operation mode.
    - Access Type: WO
  - **TWAI_ACCEPTANCE_CODE_0**: Stored the Oth byte of the filter code in reset mode.
    - Access Type: R/W

- **Register 31.6. TWAI_DATA_1_REG (0x0044)**
  - **TWAI_TX_BYTE_1**: Stored the 1st byte information of the data to be transmitted in operation mode.
    - Access Type: WO
  - **TWAI_ACCEPTANCE_CODE_1**: Stored the 1st byte of the filter code in reset mode.
    - Access Type: R/W

**Footer Information:**
- Page number and document version:
  - "1216 ESP32-S3 TRM (Version 1.7)"
- Company name at bottom left corner:
  - Espressif Systems
- Link for submitting documentation feedback:
  - Submit Documentation Feedback