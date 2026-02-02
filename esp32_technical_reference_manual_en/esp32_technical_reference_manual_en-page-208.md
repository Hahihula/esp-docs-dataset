**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Section Titles and Content:**

1. **Register Description:** 
   - Register Name: RTC_CNTL_EXT_WAKEUP_CONF_REG (0x0060)
   - Binary Representation Diagram:
     ```
     31 | 30 | 29
     -------------------
     0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0
     -------------------
     ```
   - Description:
     - RTC_CNTL_EXT_WAKEUP1_LV: external wake-up at low level, 1: external wake-up at high level. (R/W)
     - RTC_CNTL_EXT_WAKEUP_Q_LV: external wake-up at low level, 1: external wake-up at high level. (R/W)

2. **Register Description:** 
   - Register Name: RTC_CNTL_SLP_REJECT_CONF_REG (0x0064)
   - Binary Representation Diagram:
     ```
     31 | 28 | 27 | 26 | 25 | 24 | 23
     -------------------
     0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0
     -------------------
     ```
   - Description:
     - RTC_CNTL_REJECT_CAUSE: Sleep reject cause. 2: GPIO; 3: SDIO (RO).
     - RTC_CNTL_DEEP_SLP_REJECT_EN: Enable reject for deep sleep. (R/W)
     - RTC_CNTL_LIGHT_SLP_REJECT_EN: Enable reject for light sleep. (R/W)
     - RTC_CNTL_SDIO_REJECT_EN: Enable SDIO reject. (R/W)
     - RTC_CNTL_GPIO_REJECT_EN: Enable GPIO reject. (R/W)

**Footer Information:** 
- Page Number: 208
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Navigation Link:**
- Submit Documentation Feedback