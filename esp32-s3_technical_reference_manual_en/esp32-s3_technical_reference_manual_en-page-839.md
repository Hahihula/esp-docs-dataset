**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**GoBack Link:** GoBack

---

**Register Section Header:**
Register 17.17. SYSTEM_RTC_FASTMEM_CONFIG_REG (0x0050)

- **Field Descriptions and Values for SYSTEM_RTC_MEM_CRC_FINISH, SYSTEM_RTC_MEM_CRC_LEN, SYSTEM_RTC_MEM_CRC_ADDR, SYSTEM_RTC_MEM_CRC_START:**

  - `SYSTEM_RTC_MEM_CRC_FINISH`: Set this bit to start the CRC of RTC memory (R/W)
  - `SYSTEM_RTC_MEM_CRC_LEN`: This field is used to set length of RTC memory for CRC based on start address. (R/W)
  - `SYSTEM_RTC_MEM_CRC_ADDR`: This field is used to set address of RTC memory for CRC. (R/W)

- **Field Description:**
  - ` SYSTEM_RTC_MEM_CRCStart`: Set this bit to start the CRC of RTC memory (R/W).

**Register Section Header:**
Register 17.18. SYSTEM_RTC_FASTMEM_CRC_REG (0x0054)

- **Field Descriptions and Values for SYSTEM_RTC_MEM_CRCRES, SYSTEM_CLK_EN:**

  - `SYSTEM_RTC_MEM_CRCRES`: This field stores the CRC result of RTC memory. (RO)
  - `SYSTEM_CLK_EN`: Set this bit to enable the system clock. (R/W)

**Register Section Header:**
Register 17.19. SYSTEM_CLOCK_GATE_REG (0x005C)

- **Field Description for SYSTEM_CLK_EN:** 
  - `SYSTEM_CLK_EN`: Set this bit to enable the system clock.

---

**Footer Information:**
Espressif Systems
839 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback