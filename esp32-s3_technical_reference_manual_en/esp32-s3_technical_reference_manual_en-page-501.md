**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Table of Registers:

| Name                          | Description                                                                                   | Address       | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|---------------|--------|
| RTC_IO_XTAL_32P_PAD_REG      | 32 kHz crystal P-pin configuration register                                                   | 0x00C0        | R/W    |
| RTC_IO_XTAL_32N_PAD_REG      | 32 kHz crystal N-pin configuration register                                                   | 0x00C4        | R/W    |
| RTC_IO_RTC_PAD17_REG         | RTC pin 17 configuration register                                                            | 0x00C8        | R/W    |
| RTC_IO_RTC_PAD18_REG         | RTC pin 18 configuration register                                                          | 0x00CC        | R/W    |
| RTC_IO_RTC_PAD19_REG         | RTC pin 19 configuration register                                                         | 0x00D0        | R/W    |
| RTC_IO_RTC_PAD20_REG         | RTC pin 20 configuration register                                                        | 0x00D4        | R/W    |
| RTC_IO_RTC_PAD21_REG         | RTC pin 21 configuration register                                                      | 0x00D8        | R/W    |
| RTC_IO_XTL_EXT_CTR_REG       | Crystal power down enable GPIO source                                                     | 0x00E0        | R/W    |
| RTC_IO_SAR_I2C_IO_REG        | I2C pin selection                                                                         | 0x00E4        | R/W    |

**Version Register:**
- RTC_IO_DATE_REG (Version control register) - Address: 0x01FC, Access: R/W

---

### Subtitle: 6.15 Registers**

#### Section Title: 6.15.1 GPIO Matrix Registers

The addresses in this section are relative to the GPIO base address provided in Table 4.3-3 in Chapter System and Memory.

**Register Description:**
- **Register 6.1. GPIO_BT_SELECT_REG (0x0000)**
  - Address: 0x0000
  - Values of bit25 to bit31 are invalid.
  
- **Register 6.2. GPIO_OUT_REG (0x0004)**
  - Address: 0x0004

**Values Explanation for GPIO_OUT_DATA_ORIG:**
- GPIO0 ~ 21 and GPIO26 ~ 31 output values in simple GPIO output mode.
- The valid bits are bit0 to bit25. Bit26 to bit31 correspond to the output values of GPIO0 ~ 21, respectively.

---

**Footer Information:**  
Espressif Systems  
Page: 501  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- Submit Documentation Feedback