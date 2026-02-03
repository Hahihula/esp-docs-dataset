**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**GoBack Link:** GoBack

**Section Header and Description with Diagrams for Registers:**

1. **Register 2.17. RTC_I2C_SCL_START_PERIOD_REG (0x001C)**
   - **Diagram Label:** RTC_I2C_SCL_START_PERIOD
   - **Binary Representation of Register Bits:**
     ```
     31  20  19  ... 8    0
     0  O  O  O  O  O  O  Reset
     ```
   - **Description:** RTC_I2C_SCL_START_PERIOD. Number of clock cycles to wait after generating a start condition.
   - **Access Type:** (R/W)

2. **Register 2.18. RTC_I2C_SCL_STOP_PERIOD_REG (0x0020)**
   - **Diagram Label:** RTC_I2C_SCL_STOP_PERIOD
   - **Binary Representation of Register Bits:**
     ```
     31  20  19  ... 8    0
     0  O  O  O  O  O  O  Reset
     ```
   - **Description:** RTC_I2C_SCL_STOP_PERIOD. Number of clock cycles to wait before generating a stop condition.
   - **Access Type:** (R/W)

**Footer:**
- Page number and document version information:
  - "344"
  - ESP32-S3 TRM (Version 1.7)
  
- Company name at the bottom left corner:
  - Espressif Systems
  
- Link for submitting documentation feedback:
  - Submit Documentation Feedback