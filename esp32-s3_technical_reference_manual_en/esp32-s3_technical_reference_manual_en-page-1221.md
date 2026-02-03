**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**GoBack Link:** GoBack

---

**Register Section:**

- **Register Name and Address:**
  - Register 31.16, TWAI_DATA_11_REG (0x006C)
  
    **Binary Representation Diagram:**
    ```
    31 | 7 | 0
    -------------------
    TWAI_TX_BYTE_11
    ```

- **Description for TWAI_TX_BYTE_11:**
  - Stored the 11th byte information of the data to be transmitted in operation mode.
  - Access Type (WO): Write Only

---

- **Register Name and Address:**
  - Register 31.17, TWAI_DATA_12_REG (0x0070)
  
    **Binary Representation Diagram:**
    ```
    31 | 7 | 0
    -------------------
    TWAI_TX_BYTE_12
    ```

- **Description for TWAI_TX_BYTE_12:**
  - Stored the 12th byte information of the data to be transmitted in operation mode.
  - Access Type (WO): Write Only

---

- **Register Name and Address:**
  - Register 31.18, TWAI_CLOCK_DIVIDER_REG (0x007C)
  
    **Binary Representation Diagram:**
    ```
    31 | 7 | 0
    -------------------
    TWAI CLOCK OFF
    ```

- **Description for TWAI_CLOCK_DIVIDER_REG:**
  - These bits are used to configure the divisor of the external CLKOUT pin. (R/W)
  
  **TWAI_CD Description:** 
  - This bit can be configured in reset mode.
  - Options:
    - `1`: Disable the external CLKOUT pin;
    - `0`: Enable the external CLKOUT pin (RO | R/W)

---

**Footer:**
- Page Number and Document Version Information
  - "Espressif Systems" 
  - "Submit Documentation Feedback"
  - "ESP32-S3 TRM (Version 1.7)"
  - Page number at bottom center is `1221`