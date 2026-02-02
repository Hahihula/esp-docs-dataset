**Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** GoBack

---

**Section Title: Register 25.5. TWAI_DATA_0_REG (0x0040)**

- **Field Name and Description:**
  - `TWAI_TX_BYTE_0`
    - **Description:** Stored the Oth byte information of the data to be transmitted under operating mode.
    - **Mode:** WO
  - **Field Name and Description:**
    - `TWAI_ACCEPTANCE_CODE_0`
      - **Description:** Stored the Oth byte of the filter code under reset mode.

**Section Title: Register 25.6. TWAI_DATA_1_REG (0x0044)**

- **Field Name and Description:**
  - `TWAI_TX_BYTE_1`
    - **Description:** Stored the 1st byte information of the data to be transmitted under operating mode.
    - **Mode:** WO
  - **Field Name and Description:**
    - `TWAI_ACCEPTANCE_CODE_1`
      - **Description:** Stored the 1st byte of the filter code under reset mode.

---

**Footer Information:**
- Page Number: 552
- Document Title: ESP32 TRM (Version 5.6)
- Company Name and Link: Espressif Systems | Submit Documentation Feedback

**Diagram Description in Image:** The image contains two diagrams, each representing a register layout for TWAI. Each diagram shows the bit positions with labels such as `TWAI_TX_BYTE_0`, `TWAI_ACCEPTANCE_CODE_0`, etc., indicating where specific data or codes are stored within the registers.

- **First Diagram:**
  - Labelled bits from left to right:
    - TWAI_TX_BYTE_0
    - (reserved)
    - TWAI ACCEPTANCE CODE_0

- **Second Diagram:**
  - Labelled bits from left to right:
    - TWAI_TX_BYTE_1
    - (reserved)
    - TWAI ACCEPTANCE_CODE_1