**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**GoBack Link:** GoBack

**Section Header:**
Register 1.8. RTC_I2C_SCL_LOW_PERIOD_REG (0x000)

**Binary Representation Diagram for Register 1.8:**
- The diagram shows a binary representation of the register with bits labeled from '31' to '0'. Some bits are marked as "Reset".

**Description and Functionality Text under Binary Representation:**
RTC_I2C_SCL_LOW_PERIOD
Number of RTC_FAST_CLK cycles when SCL == 0. (R/W)

**Section Header:**
Register 1.9. RTC_I2C_CTRL_REG (0x004)

**Binary Representation Diagram for Register 1.9:**
- The diagram shows a binary representation with bits labeled from '31' to '0'. Some sections are marked as "Reset".

**Description and Functionality Text under Binary Representation of Register 1.9:**

- RTC_I2C_RX_LSB_FIRST
Receive LSB first. (R/W)

- RTC_I2C_TX_LSB_FIRST
Send LSB first. (R/W)

- RTC_I2C_TRANS_START
Force to generate a start condition. (R/W)

- RTC_I2C_MS_MODE
Master (1), or slave (0). (R/W)

- RTC_I2C_SCL FORCE_OUT
SCL is push-pull (1) or open-drain (0). (R/W)

- RTC_I2C_SDA FORCE_OUT
SDA is push-pull (1) or open-drain (0). (R/W)

**Footer:**
Espressif Systems

**Page Number and Document Version Information:** 
50 ESP32 TRM (Version 5.6)

**Link for Submitting Documentation Feedback:** Submit Documentation Feedback