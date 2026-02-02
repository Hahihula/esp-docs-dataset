**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**GoBack Link:** GoBack

---

**Section Header:**
Register 1.12. RTC_I2C_SLAVE_ADDR_REG (0x010)

**Binary Representation Diagram of Register:**
- The diagram shows a binary representation with bits labeled from top to bottom as follows:
  - Bit positions are numbered, starting at the rightmost bit and going left.
  - Bits range in value between '0' or '1'.
  
**Register Description Texts:** 
- RTC_I2C_SLAVE_ADDR_10BIT: Set if local slave address is 10-bit. (R/W)
- RTC_I2C_SLAVE_ADDR: Local slave address. (R/W)

---

**Section Header:**
Register 1.13. RTC_I2C_INT_CLR_REG (0x024)

**Binary Representation Diagram of Register:**
- The diagram shows a binary representation with bits labeled from top to bottom as follows:
  - Bit positions are numbered, starting at the rightmost bit and going left.
  - Bits range in value between '0' or '1'.
  
**Register Description Texts:** 
- RTC_I2C_TIME_OUT_INT_CLR: Clear interrupt upon timeout. (R/W)
- RTC_I2CTransComplete_INT_CLR: Clear interrupt upon detecting a stop pattern. (R/W)
- RTC_I2C_MASTER_TRANSComplete_INT_CLR: Clear interrupt upon completion of transaction, when in master mode. (R/W)
- RTC_I2C_ARBTRATION_LOST_INT_CLR: Clear interrupt upon losing control of the bus, when in master mode. (R/W)
- RTC_I2C_SLAVETransComplete_INT_CLR: Clear interrupt upon completion of transaction, when in slave mode. (R/W)

---

**Footer Information:** 
Espressif Systems
Page Number 52
ESP32 TRM (Version 5.6)