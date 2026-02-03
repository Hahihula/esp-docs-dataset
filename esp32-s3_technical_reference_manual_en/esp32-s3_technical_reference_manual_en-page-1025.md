**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** GoBack

---

### Register Section:

#### Register 27.16:
- **Name:** I2C_CLK_CONF_REG (0x0054)
- **Description and Bits:**
  - `I2C_SCLK_DIV_NUM`: The integral part of the divisor.
    - Access Type: Read/Write
  - `I2C_SCLK_DIV_A`: The numerator of the divisor's fractional part. 
    - Access Type: Read/Write
  - `I2C_SCLK_DIV_B`: The denominator of the divisor's fractional part.
    - Access Type: Read/Write
  - `I2C_SCLK_SEL`: The clock selection bit for I2C controller:
    - Values: XTAL_CLK, RC_FAST_CLK (Read/Write)
  - `I2C_SCLK_ACTIVE`: The clock switch bit for the I2C controller.
    - Access Type: Read/Write

#### Register 27.17:
- **Name:** I2C_SCL_SP_CONF_REG (0x0080)

---

### Register Section:

#### Register 27.16 Continued with Bits Description and Values:
- `I2C_SDA_PD_EN`: The power down enable bit for the I2C output SDA line.
  - Access Type: Read/Write
- `I2C_SCL_RST_SLV_EN`: When the master is idle, set this bit to send out SCL pulses. 
  - Description of number of pulses equals to I2C_SCL_RSTSLV_NUM[4:0].
  - Access Type: Read/Write

#### Register 27.16 Continued with Bits Description and Values:
- `I2C_SCL_RST_SLV_NUM`: Configures the pulses of SCL generated in master mode.
  - Valid when I2C_SCL_RST_SLV_EN is set to 1 (Read/Write)
- `I2C_SCL_PD_EN`: The power down enable bit for the I2C output SCL line:
  - Values: Not powered; Powered
- `I2C_SDA_PD_EN`: The power down enable bit for the I2C output SDA line.
  - Access Type: Read/Write

---

**Footer Information:** 
Espressif Systems  
1025  
ESP32-S3 TRM (Version 1.7)  

**Links and Actions:**
- Submit Documentation Feedback