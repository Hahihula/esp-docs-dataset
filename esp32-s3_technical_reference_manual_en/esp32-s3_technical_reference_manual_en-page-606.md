**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Menu:**
GoBack

**Register Information:**
- **Register Name:** Register 10.24. RTC_CNTL_RTC_SLP_REJECT_CONF_REG (0x0068)
- **Field Description and Values:**
  - `RTC_CNTL_DEEP_SLP_REJECT_EN`  
    - Bits [31, 30]: Reserved
    - Bit [29]: Reset to '0'
  - `RTC_CNTL_RTC_SLEEP_REJECT_EN`
    - Bits [12, 11]: Reserved
    - Bit [10]: Reset to '0'
  - `RTC_CNTL_LIGHT_SLP_REJECT_EN`
    - Bits [8, 7]: Reserved
    - Bit [6]: Reset to '0'

**Field Descriptions:**
- **RTC_CNTL_RTC_SLEEP_REJECT_ENA:** Set this bit to enable reject-to-sleep. (R/W)
- **RTC_CNTL_LIGHT_SLP_REJECT_EN:** Set this bit to enable reject-to-light-sleep. (R/W)
- **RTC_CNTL_DEEP_SLP_REJECT_EN:** Set this bit to enable reject-to-deep-sleep. (R/W)

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7) 
Submit Documentation Feedback