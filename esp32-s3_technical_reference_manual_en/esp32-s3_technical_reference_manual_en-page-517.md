**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** GoBack

---

**Register Section Header:**

- **Register Name**: Register 6.41. RTC_GPIO_OUT_REG (0x0000)
  - **Description**: 
    - Bit10 corresponds to GPIO0.
    - Bit11 corresponds to GPIO1, etc.

- **Bit Description Table for Register 6.41:**
  ```
  |   | 10 | 9 | ... | 0 |
  |---|----|--|-----|
  | 0 | O  | O |     | O |
  ```

**Register Section Header:**

- **Register Name**: Register 6.42. RTC_GPIO_OUT_W1TS_REG (0x004)
  - **Description**: 
    - The value written to a bit here will set the corresponding bit in RTC_GPIO_OUT_REG to be cleared.

- **Bit Description Table for Register 6.42:**
  ```
  |   | 10 | 9 | ... | 0 |
  |---|----|--|-----|
  | 0 | O  | O |     | O |
  ```

**Register Section Header:**

- **Register Name**: Register 6.43. RTC_GPIO_OUT_W1TC_REG (0x008)
  - **Description**: 
    - The value written to a bit here will clear the corresponding bit in RTC_GPIO_OUT_REG.

- **Bit Description Table for Register 6.43:**
  ```
  |   | 10 | 9 | ... | 0 |
  |---|----|--|-----|
  | 0 | O  | O |     | O |
  ```

**Footer Information:** 
Espressif Systems
Submit Documentation Feedback

**Document Version**: ESP32-S3 TRM (Version 1.7)