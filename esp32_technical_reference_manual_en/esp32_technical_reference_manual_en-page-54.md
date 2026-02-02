**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**GoBack Link:** GoBack

**Register Information and Description:**

- **Register Name:** RTC_I2C_SDA_DUTY_REG (0x030)
  - **Description:** 
    - **Field:** RTC_I2C_SDA_DUTY
      - **Type:** Number of RTC_FAST_CLK cycles between the SDA switch and the falling edge of SCL. (R/W)

- **Register Name:** RTC_I2C_SCL_HIGH_PERIOD_REG (0x038)
  - **Description:**
    - **Field:** RTC_I2C_SCL_HIGH_PERIOD
      - **Type:** Number of RTC_FAST_CLK cycles when SCL == 1. (R/W)

- **Register Name:** RTC_I2C_SCL_START_PERIOD_REG (0x040)
  - **Description:**
    - **Field:** RTC_I2C_SCL_START_PERIOD
      - **Type:** Number of RTC_FAST_CLK cycles to wait before generating a start condition. (R/W)

**Footer Information:**
- Page number and document version:
  - "54 ESP32 TRM (Version 5.6)"
  
- Company name:
  - Espressif Systems

- Links for additional actions:
  - Submit Documentation Feedback