**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**GoBack Link:** GoBack

---

**Section Header:**
Register 9.29. RTC_CNTL_DIG_ISO_REG (0x0088)

**Continuation Note:**
Continued from the previous page...

**Field Descriptions and Values for Register 9.29 - RTC_CNTL_DIG_ISO_REG**

- **RTC_CNTL_REG_RTC_CNTL_DG_PAD_AUTOHOLD_EN:** Digital pad enable auto-hold.
  - (R/W)
  
- **RTC_CNTL_CLR_RTC_CNTL_DG_PAD_AUTOHOLD:** Write-only register clears digital pad auto-hold.
  - (WO)

- **RTC_CNTL_DG_PAD_AUTOHOLD:** Read-only register indicates digital pad auto-hold status. 
  - (RO)

---

**Section Header:**
Register 9.30. RTC_CNTL_WDTCONFIGO_REG (0x008C)

**Field Descriptions and Values for Register 9.30 - RTC_CNTL_WDTCONFIGO_REG**

- **Field Name:** RTC_CNTL_WDT_EN
  - Description: Enable RTC WDT.
  - Access Type: Read/Write
  
- **Field Name:** RTC_CNTL_WDT_STGO
  - Description: Interrupt stage enable, CPU reset stage enable. 
  - Access Type: Read/Write

- **Field Name:** RTC_CNTL_WDT_STG1
  - Description: Interrupt stage enable.
  - Access Type: Read/Write
  
- **Field Name:** RTC_CNTL_WDT_STG2
  - Description: Interrupt stage enable, CPU reset stage enable. 
  - Access Type: Read/Write

- **Field Name:** RTC_CNTL_WDT_STG3
  - Description: Interrupt stage enable.
  - Access Type: Read/Write
  
- **Field Name:** RTC_CNTL_WDT_APPCPU_RESET_EN
  - Description: RTC WDT reset APP_CPU enable. 
  - Access Type: Read/Write

- **Field Name:** RTC_CNTL_WDT_PROCPU_RESET_EN
  - Description: RTC WDT reset PRO_CPU enable.
  - Access Type: Read/Write
  
- **Field Name:** RTC_CNTL_WDT_FLASHBOOT_MOD_EN
  - Description: Enable RTC WDT in flash boot. 
  - Access Type: Read/Write

- **Field Name:** RTC_CNTL_WDT_SYS_RESET_LENGTH
  - Description: System reset counter length, unit: RTC_SLOW_CLK cycle.
  - Range: The value can be 0 ~ 7 (R/W)
  
- **Field Name:** RTC_CNTL_WDT_CPU_RESET LENGTH
  - Description: CPU reset counter length, unit: RTC_SLOW_CLK cycle. 
  - Range: The value can be 0 ~ 7 (R/W)

---

**Footer Information:**
Espressif Systems

**Document Version and Submission Link:**
ESP32 TRM (Version 5.6)
Submit Documentation Feedback