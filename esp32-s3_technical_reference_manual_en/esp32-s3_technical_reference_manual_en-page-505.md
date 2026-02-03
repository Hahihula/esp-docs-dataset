**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** GoBack

---

**Register Section Header:**

- **Register Name**: Register 6.12. GPIO_ENABLE1_REG (0x002C)
  - **Description**: 
    - **Field**: GPIO_ENABLE_DATA
      - **Type**: reserved
    - **Address**: 31, 22, 21, D
    - **Value**: 0x0000

- **Register Name**: GPIO ENABLE1 DATA GPIO32 ~ 48 output enable register. (R/W)

---

**Register Section Header:**

- **Register Name**: Register 6.13. GPIO_ENABLE1_W1TS_REG (0x0030)
  - **Description**: 
    - **Field**: GPIO_ENABLE_DATA
      - **Type**: reserved

- **Register Name**: GPIO ENABLE1 WITS GPIO32 ~ 48 output enable set register.
  - If the value 1 is written to a bit here, the corresponding bit in GPIO_ENABLE1_REG will be set to 1. Recommended operation: use this register to set GPIO_ENABLE1_REG.

---

**Register Section Header:**

- **Register Name**: Register 6.14. GPIO ENABLE1_W1TC_REG (0x0034)
  - **Description**: 
    - **Field**: GPIO_ENABLE_DATA
      - **Type**: reserved

- **Register Name**: GPIO ENABLE1 W1TC GPIO32 ~ 48 output enable clear register.
  - If the value 1 is written to a bit here, the corresponding bit in GPIO_ENABLE1_REG will be cleared. Recommended operation: use this register to clear GPIO_ENABLE1_REG.

---

**Footer Information:** 
- **Company**: Espressif Systems
- **Document Version**: ESP32-S3 TRM (Version 1.7)
- **Page Number**: 505

**Feedback Link**: Submit Documentation Feedback