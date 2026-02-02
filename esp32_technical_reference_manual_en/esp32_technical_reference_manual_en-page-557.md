**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** GoBack

---

### Register Section:

- **Register Name and Address:**
  - TWAI_DATA_11_REG (0x006C)
  
  **Description of the register contents in binary format with labels for specific bits or fields.**

- **Register Name and Address:**
  - TWAI_DATA_12_REG (0x0070)

  **Description of the register contents in binary format with labels for specific bits or fields.**

- **Register Name and Address:**
  - TWAI_TX_BYTE_11

  **Description:** Stored the 11th byte information of the data to be transmitted under operating mode.

- **Register Name and Address:**
  - TWAI_TX_BYTE_12

  **Description:** Stored the 12th byte information of the data to be transmitted under operating mode.

### Register Section:

- **Register Name and Address:**
  - TWAI_CLOCK_DIVIDER_REG (0x007C)

  **Description in binary format with labels for specific bits or fields.**

  **Field Descriptions:**  
  - TWAI_CD
    - These bits are used to configure frequency dividing coefficients of the external CLKOUT pin.
    - Access: Read/Write
  
  - TWAI_CLOCK_OFF
    - This bit can be configured under reset mode:
      - 1: Disable the external CLKOUT pin; 
      - 0: Enable the external CLKOUT pin (Read Only)
  
  - TWAI_EXT_MODE
    - This bit can be configured under reset mode.
    - 1: Extended mode, compatible with CAN2.0B;
    - 0: Basic mode

---

**Footer Information:**  
Espressif Systems  
557  
Submit Documentation Feedback  

ESP32 TRM (Version 5.6)