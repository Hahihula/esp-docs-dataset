**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
Register 26.54, UHCI_ESC_CONFO_REG (0x0070)

**Field Description Table for Register 26.54:**

- **Field Name:** UHCI_SEPER_CHAR
  - **Description:** This field is used to define separators to encode data packets.
  - **Default Value:** OxCO
  - **Access Mode:** (R/W)
  
- **Field Name:** UHCI_SEPER_ESC_CHA0
  - **Description:** This field is used to define the first character of SLIP escape sequence.
  - **Default Value:** OxDB
  - **Access Mode:** (R/W)

- **Field Name:** UHCI_SEPER_ESC_CHA1
  - **Description:** This field is used to define the second character of SLIP escape sequence.
  - **Default Value:** OxDC
  - **Access Mode:** (R/W)

**Section Header:**
Register 26.55, UHCI_ESC_CONFI_REG (0x0074)

**Field Description Table for Register 26.55:**

- **Field Name:** UHCI_ESC_SEQO
  - **Description:** This field is used to define a character that need to be encoded.
  - **Default Value:** OxDB
  - **Access Mode:** (R/W)
  
- **Field Name:** UHCI_ESC_SEQO_CHA0
  - **Description:** This field is used to define the first character of SLIP escape sequence.
  - **Default Value:** OxDB
  - **Access Mode:** (R/W)

- **Field Name:** UHCI_ESC_SEQO_CHA1
  - **Description:** This field is used to define the second character of SLIP escape sequence.
  - **Default Value:** OxDD
  - **Access Mode:** (R/W)

**Footer:**
Espressif Systems  
976 ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- Submit Documentation Feedback

(Note: The image contains a diagram with binary values and labels, but it is not described in detail as per the instructions.)