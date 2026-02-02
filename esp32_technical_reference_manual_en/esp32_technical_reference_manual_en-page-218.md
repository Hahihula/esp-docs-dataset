**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**GoBack Link:** GoBack

---

**Section Header: Register 9.31**

- **Title:** RTC_CNTL_WDTCONFIGn_REG  
  - Description: n : 1-4 (0x008C+4*n)  
  - Address: 0x000000FFF
  - Bit Description:
    - RTC_CNTL_WDTCONFIGn: Hold cycles for WDT stage n. (R/W)

---

**Section Header: Register 9.32**

- **Title:** RTC_CNTL_WDTFEED_REG  
  - Address: 0x00A0

- **Bit Description Table:**
  - Bit Positions:
    - 31 to 30
      - Value (hex): 0x00
      - Description: reserved
  
  - Bits from position 29 down are not specified in the visible part of the image.

---

**Section Header: Register 9.33**

- **Title:** RTC_CNTL_WDT_FEED  
  - Description: SW feeds WDT. (WO)

- Address for this register is also mentioned but it's partially cut off, only "0x05D83AA1" visible.
  
- Bit Description:
  - Bit Position and Value not specified in the image.

---

**Section Header: Register 9.34**

- **Title:** RTC_CNTL_WDTWPROTECT_REG
  - Description: If the register contains a different value than 0x50d83aa1, write protection for the RTC watchdog (RWDT) is enabled. (R/W)

---

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32 TRM (Version 5.6)
- Page Number: 218

**Link:** Submit Documentation Feedback