**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header:**
GoBack

**Register Information Section:**

- **Title:** Register 6.44. RTC_GPIO_ENABLE_REG (0x000C)
  - Description:
    - "RTC_GPIO_ENABLE_GPIOO ~ 21 output enable. Bit10 corresponds to GPIO0, bit11 corresponds to GPIO1, etc. If the bit is reset to 1, it means this GPIO pin is output."
    - Access: (R/W)

- **Title:** Register 6.45. RTC_GPIO_ENABLE_W1TS_REG (0x0010)
  - Description:
    - "RTC_GPIO_ENABLE_W1TS GPIOO ~ 21 output enable set register. If the value 1 is written to a bit here, the corresponding bit in RTC_GPIO_ENABLE_REG will be set to 1."
    - Recommended operation: use this register to set RTC_GPIO_ENABLE_REG.
    - Access: (WO)

- **Title:** Register 6.46. RTC_GPIO_ENABLE_W1TC_REG (0x0014)
  - Description:
    - "RTC_GPIO_ENABLE_W1TC GPIOO ~ 21 output enable clear register. If the value 1 is written to a bit here, the corresponding bit in RTC_GPIO_ENABLE_REG will be cleared."
    - Recommended operation: use this register to clear RTC_GPIO_ENABLE_REG.
    - Access: (WO)

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 518

**Navigation Links:**
- Submit Documentation Feedback