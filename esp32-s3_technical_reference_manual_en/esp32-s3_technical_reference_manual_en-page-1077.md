**Title: Chapter 28 I2S Controller (I2S)**

---

**Section Title: Register 28.21. I2S_CONF_SINGE_DATA_REG (0x068)**

- **Field Name:** `I2S_SINGLE_DATA`
  - Description: The configured constant channel data to be sent out.
  - Access Rights: Read/Write
  - Reset Value: 0

---

**Section Title: Register 28.22. I2S_STATE_REG (0x006C)**

- **Field Name:** `I2S_TX_IDLE`
  - Description:
    - Bit 1 to bit 31 are reserved.
    - Bit 0 indicates the state of the I2S TX unit: 
      - Value '1': I2S TX unit is in idle state
      - Value '0': I2S TX unit is working

---

**Section Title: Register 28.23. I2S_DATE_REG (0x0080)**

- **Field Name:** `I2S_DATE`
  - Description:
    - Bit 31 to bit 27 are reserved.
    - Bits from position '0' and onwards represent the date in a specific format: 
      - Value: "0x2009070" (Reset value)

---

**Section Title: I2S_DATE Version control register. (R/W)**

- **Field Name:** `I2S_DATE`
  - Description:
    - This is used for versioning purposes.

---

**Footer Information:**
- Company: Espressif Systems
- Document Page Number: 1077
- Document Title: ESP32-S3 TRM (Version 1.7)
- Link Texts: "Submit Documentation Feedback" and a link labeled as "GoBack".