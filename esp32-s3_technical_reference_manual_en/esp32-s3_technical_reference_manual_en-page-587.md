**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Subtitle:**
10.8 Registers

**Body Text:**
The addresses in this section are relative to low-power management base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table Title:**
Register 10.1. RTC_CNTL_RTC_OPTIONSO_REG (0x0000)

**Table Content Description:**
A table with various register addresses, their descriptions, bit fields for configuration or reset actions related to CPU stall settings, I2C force pins, PLL force pin configurations.

- **Example Entries from Table:**
  - `RTC_CNTL_SWSTALL_APPCPU_CO`: When RTC_CNTL_SWSTALL_APPCPU_C1 is configured to 0x21, setting this field to 0x2 stalls the CPU1 by SW. (R/W)
  - `RTC_CNTL_BB_I2C FORCE_PD`: Set this bit to FPD BB_I2C. (R/W)

**Footer:**
Continued on the next page...

**Additional Information at Bottom of Page:**
Espressif Systems
587 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback