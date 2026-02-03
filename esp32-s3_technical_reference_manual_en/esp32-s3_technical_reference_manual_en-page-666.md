**Title:**
Chapter 12 Timer Group (TIMG)

**Body Text and Descriptions of Registers:**

- **Register 12.12. TIMG_WDTCONFIG2_REG (0x0050)**
  - Description:
    ```
    TIMG_WDT_STGO_HOLD
    Stage 0 timeout value, in MWDT clock cycles. (R/W)
    ```
  - Value: `26000000`
  - Reset Value: `0`

- **Register 12.13. TIMG_WDTCONFIG3_REG (0x0054)**
  - Description:
    ```
    TIMG_WDT_STG1_HOLD
    Stage 1 timeout value, in MWDT clock cycles. (R/W)
    ```
  - Value: `0x7ffffff`
  - Reset Value: `0`

- **Register 12.14. TIMG_WDTCONFIG4_REG (0x0058)**
  - Description:
    ```
    TIMG_WDT_STG2_HOLD
    Stage 2 timeout value, in MWDT clock cycles. (R/W)
    ```
  - Value: `0xffffff`
  - Reset Value: `0`

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
- Submit Documentation Feedback

**Page Number:** 
666