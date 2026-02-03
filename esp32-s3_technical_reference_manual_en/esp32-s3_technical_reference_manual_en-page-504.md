**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Menu:**
GoBack

---

**Section Title:**
Register 6.9. GPIO_ENABLE_REG (0x0020)

**Body Text:**
- **Label:** GPIO_ENABLE_DATA
- **Description:** GPIO0~31 output enable register.
- **Access Mode:** R/W

**Diagram/Visualization Description:**
- A horizontal line with a label "Reset" on the right end.

---

**Section Title:**
Register 6.10. GPIO_ENABLE_W1TS_REG (0x0224)

**Body Text:**
- **Label:** GPIO ENABLE WITS
- **Description:** 
  - **Text:** If the value 1 is written to a bit here, the corresponding bit in GPIO_ENABLE_REG will be set to 1.
  - **Recommended Operation:** use this register to set GPIO_ENABLE_REG. (WO)

---

**Section Title:**
Register 6.11. GPIO_ENABLE_W1TC_REG (0x0228)

**Body Text:**
- **Label:** GPIO ENABLE W1TC
- **Description:**
  - If the value 1 is written to a bit here, the corresponding bit in GPIO_ENABLE_REG will be cleared.
  - Recommended operation: use this register to clear GPIO_ENABLE_REG. (WO)

---

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)