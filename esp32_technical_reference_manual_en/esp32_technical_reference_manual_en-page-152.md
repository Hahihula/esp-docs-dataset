**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** GoBack

---

**Section Header: Register 6.41. RTCIO_RTC_GPIO_STATUS_REG (0x0018)**

- **Binary Representation Table:**
  - Bit positions are labeled from right to left.
  
- **Description:**
  - `RTCIO_RTC_GPIO_STATUS_INT GPIO0-17 interrupt status.`
  - "Bit14 is GPIO[0], bit15 is GPIO[1], etc."
  - This register should be used together with `RTCIO_RTC_GPIO_PINn_INT_TYPE` in `RTCIO_RTC_GPIO_PINn_REG`.
  - `1`: corresponding interrupt; `0`: no interrupt. (R/W)

---

**Section Header: Register 6.42. RTCIO_RTC_GPIO_STATUS_W1TS_REG (0x001C)**

- **Binary Representation Table:**
  - Bit positions are labeled from right to left.
  
- **Description:**
  - `RTCIO_RTC_GPIO_STATUS_INT_GPIO0-17 interrupt set register.`
  - "For every bit that is 1 in the value written here, the corresponding bit in RTCIO_RTC_GPIO_STATUS_INT will be set." (WO)

---

**Section Header: Register 6.43. RTCIO_RTC_GPIO_STATUS_W1TC_REG (0x0020)**

- **Binary Representation Table:**
  - Bit positions are labeled from right to left.
  
- **Description:**
  - `RTCIO_RTC_GPIO_STATUS_INT_GPIO0-17 interrupt clear register.`
  - "For every bit that is 1 in the value written here, the corresponding bit in RTCIO_RTC_GPIO_STATUS_INT will be cleared." (WO)

---

**Footer Information:** 
- Page number: 152
- Document version and company information:
  - ESP32 TRM (Version 5.6)
  - Espressif Systems

- **Action Links:**
  - Submit Documentation Feedback