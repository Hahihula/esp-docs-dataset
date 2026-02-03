**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section Heading:**
27.8 Registers

**Body Text:**
The addresses in this section are relative to I2C Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection Title:**
Register 27.1. I2C_SCL_LOW_PERIOD_REG (0x0000)

**Description of Register:**
I2C_SCL_LOW_PERIOD This field is used to configure how long SCL remains low in master mode, in I2C module clock cycles. (R/W)

**Binary Representation Diagram for Register 27.1:** 
[Binary representation diagram showing the bits labeled as reserved and reset]

**Subsection Title:**
Register 27.2. I2C_SDA_HOLD_REG (0x0030)

**Description of Register:**
I2C_SDA_HOLD_TIME This field is used to configure the time to hold the data after the falling edge of SCL, in I2C module clock cycles. (R/W)

**Binary Representation Diagram for Register 27.2:** 
[Binary representation diagram showing the bits labeled as reserved and reset]

**Subsection Title:**
Register 27.3. I2C_SDA_SAMPLE_REG (0x0034)

**Description of Register:**
I2C_SDA_SAMPLE_TIME This field is used to configure how long SDA is sampled, in I2C module clock cycles. (R/W)

**Binary Representation Diagram for Register 27.3:** 
[Binary representation diagram showing the bits labeled as reserved and reset]

**Footer Information:**
Espressif Systems
1018 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback