**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** GoBack

---

**Section Header: Register Information**

- **Register Name and Address:**
  - TWAI_ARB_LOST_CAP_REG (0x002C)
    - Description:
      ```
      TWAI_ARB_LOST_CAP This register contains information about the bit position of lost arbitration.
      (RO)
      ```

- **Register Name and Address:**
  - TWAI_ERR_CODE_CAP_REG (0x0030)
    - Fields in Binary Format with Labels:
      ```
      31 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8
      (reserved) TWAI_ERR_CODE_TYPE TWAI_ERR_CODE_DIRECTION TWAI_ERR_CODE_SEGMENT
      ```
    - Description:
      ```
      TWAI_ERR_CODE This register contains information about the bit position of lost arbitration.
      ```

- **Register Name and Address:**
  - TWAI_ECC_SEGMENT (25.5)
    - Description:
      ```
      TWAI_ECC_SEGMENT This register contains information about the location of errors, see Table
      25.5-11 for details. (RO)
      ```

- **Register Name and Address:**
  - TWAI_ECC_DIRECTION (25.5)
    - Description:
      ```
      TWAI_ECC_DIRECTION This register contains information about transmission direction of the node when error occurs.
      1: Error occurs when receiving a message; 0: Error occurs when transmitting a message
      ```

- **Register Name and Address:**
  - TWAI_ECC_TYPE (25.5)
    - Description:
      ```
      TWAI_ECC_TYPE This register contains information about error types: 00: bit error; 01: form error;
      10: stuff error; 11: other type of error
      ```

- **Register Name and Address:**
  - TWAI_RX_ERR_CNT_REG (0x0038)
    - Fields in Binary Format with Labels:
      ```
      31 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10
      (reserved) TWAI_RX_ERR_CNT
      ```
    - Description:
      ```
      TWAI_RX_ERR_CNT The RX error counter register, reflects value changes under reception status.
      ```

**Footer:**
- Company Name and Document Version Information:
  - Espressif Systems ESP32 TRM (Version 5.6)
  
- Navigation Links:
  - Submit Documentation Feedback