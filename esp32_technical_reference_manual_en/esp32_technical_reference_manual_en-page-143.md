**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

**Section Title:** GPIO_STATUS1_REG  
**Register Number:** 6.19  
**Register Name:** GPIO_STATUS1_REG (0x0050)  

- **Description:**  
  - **Field Name:** GPIO_STATUS1_INT  
    - **Type:** GPIO32-39 interrupt status register.
    - Each bit can be either of the two interrupt sources for the two CPUs. The enable bits in GPIO_PINn_INT_ENA, corresponding to the 13-16 bits in GPIO_PINn_REG should be set to 1.

**Field Description:**
- **Reset Value:** 0

---

**Section Title:** Register  
**Register Number:** 6.20  
**Register Name:** GPIO_STATUS1_W1TS_REG (0x0054)  

- **Description:**  
  - **Field Name:** GPIO_STATUS1_INT_W1TS  
    - **Type:** GPIO32-39 interrupt status set register.
    - For every bit that is 1 in the value written here, the corresponding bit in GPIO_STATUS1_INT will be set.

**Field Description:**
- **Reset Value:** 0

---

**Section Title:** Register  
**Register Number:** 6.21  
**Register Name:** GPIO_STATUS1_W1TC_REG (0x0058)  

- **Description:**  
  - **Field Name:** GPIO_STATUS1_INT_W1TC  
    - **Type:** GPIO32-39 interrupt status clear register.
    - For every bit that is 1 in the value written here, the corresponding bit in GPIO_STATUS1_INT will be cleared.

**Field Description:**
- **Reset Value:** 0

---

**Section Title:** Register  
**Register Number:** 6.22  
**Register Name:** GPIO_ACPU_INT_REG (0x0060)  

- **Description:**  
  - **Field Name:** GPIO_ACPU_INT_REG  
    - **Type:** GPIO31 APP CPU interrupt status.
    - Read-only.

**Field Description:**
- **Reset Value:** 0

---

**Footer Information:**  
Espressif Systems  
Page Number: 143  
Document Version: ESP32 TRM (Version 5.6)  

**Action Links:** Submit Documentation Feedback