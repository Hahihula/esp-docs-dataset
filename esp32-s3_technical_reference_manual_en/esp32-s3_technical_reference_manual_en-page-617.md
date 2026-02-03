**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**GoBack Link:** GoBack

**Register Information and Descriptions:**

- **Register Name:** RTC_CNTL_RTC_CPUSTALL_REG (0x00BC)
  - **Field Description:**
    - `RTC_CNTL_SWSTALL_APPCPU_C1`
      - **Bits:** 31 to 26
      - **Description:** Set this bit to allow the SW to be able to send the CPUO into stalling. (R/W)

- **Register Name:** RTC_CNTL_RTC_STALL_PROCPU_C1
  - **Bits:** 0 and 19 onwards, with bits from 25 down to 31 being reserved.
  - **Description:** Set this bit to allow the SW to be able to send the CPU1 into stalling. (R/W)

- **Register Name:** RTC_CNTL_RTC_STORE4_REG (0x00C0)
  - **Field Description:**
    - `RTC_CNTL_RTC_SCRATCH4`
      - **Bits:** 31 onwards
      - **Description:** Retention register 4. (R/W)

- **Register Name:** RTC_CNTL_RTC STORE5_REG (0x00C4)
  - **Field Description:**
    - `RTC_CNTL_RTC_SCRATCH5`
      - **Bits:** 31 to the end of the field
      - **Description:** Retention register 5. (R/W)

**Footer Information:**
- Page Number: 617
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name and Link for Feedback:
  - Espressif Systems
  - Submit Documentation Feedback

(Note: The image contains diagrams with binary representations, but they are not described in detail as per the instructions.)