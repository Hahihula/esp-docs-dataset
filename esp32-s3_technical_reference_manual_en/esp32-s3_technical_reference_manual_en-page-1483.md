**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

### Section Header:
Register 39.4. RTC_CNTL_TOUCH_SLP_THRES_REG (0x0114)

**Diagram Description:**
- A horizontal bar diagram with labels indicating different bits of the register.
- Bits are labeled as follows from left to right, starting at bit position `27` and ending at bit position `31`: 
  - RTC_CNTL_TOUCH_SLP_PAD
  - RTC_CNTL TOUCH SLEEP APPROACH EN (reserved)
  - RTC_CNTL TOUCH SLEEP THRES
  - RTC_CNTL TOUCH SLEEP PAD

**Register Description:**
- **Field:** RTC_CNTL_TOUCH_SLP_THRES
  - **Description:** Set the threshold for sleep touch pin. (R/W)

- **Field:** RTC_CNTL_TOUCH_SLP_APPROACH_EN
  - **Description:** Enable the proximity mode of touch sleep pin. (R/W)

- **Field:** RTC_CNTL TOUCH SLEEP PAD
  - **Description:** Select sleep pin. (R/W)

---

### Section Header:
Register 39.5. RTC_CNTL_TOUCH_APPROACH_REG (0x0118)

**Diagram Description:**
- Another horizontal bar diagram with labels indicating different bits of the register.
- Bits are labeled as follows from left to right, starting at bit position `24` and ending at bit position `31`: 
  - RTC_CNTL TOUCH SLEEP APPROACH MEAS TIME
  - RTC_CNTL TOUCH SLEEP CHANNEL CLR (reserved)

**Register Description:**
- **Field:** RTC_CNTL_TOUCH_SLP_CHANNEL_CLR
  - **Description:** Clear touch sleep channel. (WO)

- **Field:** RTC_CNTL_TOUCH_APPROACH_MEAS_TIME
  - **Description:** Set the total measurement times for the pins in proximity mode. Range: `0 ~ 255`. (R/W)

---

**Footer Information:**
Espressif Systems  
Page Number: 1483  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- Submit Documentation Feedback