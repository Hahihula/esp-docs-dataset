**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** GoBack

---

**Section Header: Register**

- **Register Name**: RTC_GPIO_STATUS_REG (0x0018)
  
  - **Description**: 
    - `RTC_GPIO_STATUS_INT` GPIO~21 interrupt status register. Bit10 corresponds to GPIO0, bit11 corresponds to GPIO1, etc.
    - This register should be used together with `RTC_GPIO_PINn_INT_TYPE` in `RTC_GPIO_PINn_REG`. 0: no interrupt; 1: corresponding interrupt.

- **Register Name**: RTC_GPIO_STATUS_WITS_REG (0x001C)

  - **Description**:
    - `RTC_GPIO_STATUS_INT_WITS` GPIO~21 interrupt set register. If the value 1 is written to a bit here, the corresponding bit in `RTC_GPIO_STATUS_INT` will be set to 1.
    - Recommended operation: use this register to set `RTC_GPIO_STATUS_INT`.

- **Register Name**: RTC_GPIO_STATUS_WITC_REG (0x0020)

  - **Description**:
    - `RTC_GPIO_STATUS_INT_WITC` GPIO~21 interrupt clear register. If the value 1 is written to a bit here, the corresponding bit in `RTC_GPIO_STATUS_INT` will be cleared.
    - Recommended operation: use this register to clear `RTC_GPIO_STATUS_INT`.

---

**Footer Information:** 
- **Company**: Espressif Systems
- **Document Version**: ESP32-S3 TRM (Version 1.7)
- **Page Number**: 519

**Feedback Link**: Submit Documentation Feedback