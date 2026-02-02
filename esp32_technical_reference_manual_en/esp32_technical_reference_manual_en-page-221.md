**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Link:**
GoBack

**Subtitle:**
Register 9.37. RTC_CNTL_EXT_WAKEUP1_REG (0x00CC)

**Body Text and Diagrams with Labels:**

- **Diagram Label:** RTC_CNTL_EXT_WAKEUP1_STATUS_CLR
  - **Description:** 
    - Bitfield representation:
      ```
      31 | 19 | 18 | 17 | 0
      -------------------
      O   O   O   O   O   O   O   (reserved)
      ```

- **Diagram Label:** RTC_CNTL_EXT_WAKEUP1_SEL
  - **Description:**
    - Bitfield representation:
      ```
      31 | 19 | 18 | 17 | 0
      -------------------
      O   O   O   O   O   O   (reserved)
      ```

- **Text Description:** 
  - RTC_CNTL_EXT_WAKEUP1_STATUS_CLR: Clear external wakeup1 status. (WO)

- **Text Description:** 
  - RTC_CNTL_EXT_WAKEUP1_SEL: Bitmap to select RTC pads for external wakeup1. (R/W)

**Subtitle:**
Register 9.38. RTC_CNTL_EXT_WAKEUP1_STATUS_REG (0x00D0)

**Body Text and Diagrams with Labels:**

- **Diagram Label:** RTC_CNTL_EXT_WAKEUP1_STATUS
  - **Description:**
    - Bitfield representation:
      ```
      31 | 19 | 18 | 17 | 0
      -------------------
      O   O   O   O   O   (reserved)
      ```

- **Text Description:** 
  - RTC_CNTL_EXT_WAKEUP1_STATUS: EXT1 wakeup source status. (RO)

**Footer Information:**
Espressif Systems  
221 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback