**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Register Information:**

- **Register Name:** Register 27.12, I2C_TO_REG (0x000C)
  
  - **Field Description:**
    - `I2C_TIME_OUT_VALUE`: This field is used to configure the timeout value for receiving a data bit in I2C_SCLK clock cycles. The configured timeout value equals \(2^{I2C_TIME_OUT_VALUE}\) clock cycles.
      - **Access:** (R/W)
      
    - `I2C_TIME_OUT_EN`: This is the enable bit for timeout control.
      - **Access:** (R/W)

- **Register Name:** Register 27.13, I2C_SLAKE_ADDR_REG (0x001D)
  
  - **Field Description:**
    - `I2C_SLAVE_ADDR`: When the I2C controller is in slave mode, this field is used to configure the slave address.
      - **Access:** (R/W)
      
    - `I2C_ADDR_10BIT_EN`: This field is used to enable the 10-bit addressing mode in master mode.
      - **Access:** (R/W)

**Footer:**
- Page number and document version information:
  - "Espressif Systems" 
  - Document page count or identifier: "1023"
  - Document title abbreviation with revision note: "ESP32-S3 TRM (Version 1.7)"
  
- Link for submitting documentation feedback.
  - Text link labeled as “Submit Documentation Feedback”