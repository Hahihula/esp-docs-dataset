**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
Register 26.56, UHCI_ESC_CONF2_REG (0x0078)

**Body Text with Table and Descriptions:**

- **Field Description:** 
  - `UHCI_ESC_SEQ1`: This field is used to define a character that needs to be encoded.
    - Default value: Ox11
    - Used as flow control character. (R/W)
  
- **Field Description:**
  - `UHCI_ESC_SEQ1_CHAR0`:
    - The default value for this register's first bit position is OxDB.

- **Field Description:** 
  - `UHCI_ESC_SEQ1_CHAR1`:
    - This field defines the second character of SLIP escape sequence.
    - Default value: OxDE

**Section Header:**
Register 26.57, UHCI_ESC_CONF3_REG (0x007C)

**Body Text with Table and Descriptions:**

- **Field Description:** 
  - `UHCI_ESC_SEQ2`: This field is used to define a character that needs to be decoded.
    - Default value: Ox13
    - Used as flow control character. (R/W)
  
- **Field Description:**
  - `UHCI_ESC_SEQ2_CHAR0`:
    - The default value for this register's first bit position is OxDB.

- **Field Description:** 
  - `UHCI_ESC_SEQ2_CHAR1`:
    - This field defines the second character of SLIP escape sequence.
    - Default value: OxDF

**Footer Information:**
Espressif Systems
Page Number: 977
Document Version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback