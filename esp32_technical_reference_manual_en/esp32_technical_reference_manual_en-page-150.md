**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** GoBack

---

**Section Header - Register Description:**

- **Register Name:** RTCIO_RTC_GPIO_OUT_REG (0x0000)
  - **Description:** 
    - Bit positions are labeled from left to right.
    - The register is described as "RTCIO_RTC_GPIO_OUT_DATA GPIOO-17 output register. Bit14 is GPIO[0], bit15 is GPIO[1], etc."
    - Access type: (R/W)

---

**Section Header - Register Description:**

- **Register Name:** RTCIO_RTC_GPIO_OUT_WITS_REG (0x0004)
  - **Description:** 
    - Bit positions are labeled from left to right.
    - The register is described as "RTCIO_RTC_GPIO_OUT_DATA_WITS GPIOO-17 output set register. For every bit that is 1 in the value written here, the corresponding bit in RTCIO_RTC_GPIO_OUT will be set."
    - Access type: (WO)

---

**Section Header - Register Description:**

- **Register Name:** RTCIO_RTC_GPIO_OUT_WITC_REG (0x0008)
  - **Description:** 
    - Bit positions are labeled from left to right.
    - The register is described as "RTCIO_RTC_GPIO_OUT_DATA_WITC GPIOO-17 output clear register. For every bit that is 1 in the value written here, the corresponding bit in RTCIO_RTC_GPIO_OUT will be cleared."
    - Access type: (WO)

---

**Footer Information:** 
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:** 150