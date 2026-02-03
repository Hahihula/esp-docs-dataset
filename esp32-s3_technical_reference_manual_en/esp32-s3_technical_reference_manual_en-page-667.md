**Title: Chapter 12 Timer Group (TIMG)**

---

### Register Descriptions:

- **Register 12.15. TIMG_WDTCONFIG5_REG (0x005C)**
  - **Field:** TIMG_WDT_STG3_HOLD, Stage 3 timeout value in MWDT clock cycles.
    - **Type:** (R/W)
    - **Reset Value:** 0

- **Register 12.16. TIMG_WDTFEED_REG (0x0060)**
  - **Field:** TIMG_WDT_FEED, Write any value to feed the MWDT.
    - **Type:** (WT)

- **Register 12.17. TIMG_WDTWPROTECT_REG (0x0064)**
  - **Field:** TIMG_WDT_WKEY
    - If the register contains a different value than its reset value, write protection is enabled.
      - **Type:** (R/W)
      - **Reset Value:** 0x50d83aa1

---

**Footer:**

- Espressif Systems
- Page Number: 667
- Document Title: ESP32-S3 TRM (Version 1.7)

[Submit Documentation Feedback](#)