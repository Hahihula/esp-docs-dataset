**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack**

---

**Register Section Header:**  
Register 6.56. RTC_IO_XTL_EXT_CTR_REG (0x0DEO)

**Binary Representation Table for Register 6.56:**
- Bits are labeled from right to left as follows:
  - Bit 31
  - Bit 27
  - Bit 26

**Text Description under Binary Table:**  
RTC_IO_XTL_EXT_CTR_SEL  
Select the external crystal power down enable source to get into sleep mode. O: select GPIO0; 1: select GPIO1, etc.

The input value on this pin XOR RTC_CNTL_EXT_XTL_CONF_REG[30] is the crystal power down enable signal. (R/W)

**Register Section Header:**  
Register 6.57. RTC_IO_SAR_I2C_IO_REG (0x0E4)

**Binary Representation Table for Register 6.57:**
- Bits are labeled from right to left as follows:
  - Bit 31
  - Bit 30

**Text Description under Binary Table:**  
RTC_IO_SAR_I2C_SDA_SEL  
Selects a pin the RTC I2C SCL signal connects to.

**Options for Register 6.57:**
- O: use RTC GPIO2.
- Use RTC GPIO1; (R/W)

**Register Section Header:**  
Register 6.58. RTC_IO_DATE_REG (0x01FC)

**Binary Representation Table for Register 6.58:**
- Bits are labeled from right to left as follows:
  - Bit 31
  - Bit 28

**Text Description under Binary Table:**  
RTC_IO_DATE  
Version control register (R/W)  

**Options for Register 6.58:**
- O: use RTC GPIO3.
- Use RTC GPIO0; (R/W)

---

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)
Page number at the bottom of page is "525"