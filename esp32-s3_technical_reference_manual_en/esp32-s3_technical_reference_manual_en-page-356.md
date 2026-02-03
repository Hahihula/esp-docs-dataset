**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**GoBack Link:** GoBack

---

**Section Header: Register 2.43. RTC_I2C_CMD15_REG (0x0074)**

- **Field Description and Bit Positions Diagram for RTC_I2C_COMMAND15:**
  - Bits [31, 30] to [14, 13]: Reserved
  - Bits [13, 0]: Command content. Reset value is `0x00`.
  
- **Field Description:** 
  - RTC_I2C_CMD15: Content of command 15.
  - For more information about the register I2C COMMAND15_REG in Chapter 12C Controller (R/W).
  - When command 15 is done, this bit changes to `1` (RO).

**Section Header: Register 2.44. RTC_I2C_DATE_REG (0x00FC)**

- **Field Description and Bit Positions Diagram for RTC_I2C_DATE:**
  - Bits [31, 28] to [27, 0]: Reserved
  - Bits [26, 0]: Version control register. Reset value is `0x195310`.

- **Field Description:** 
  - RTC_I2C_DATE: Version control register (R/W).

---

**Footer Information:**
Espressif Systems  
Page Number: 356  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link for Submitting Documentation Feedback: [Submit Documentation Feedback](#)