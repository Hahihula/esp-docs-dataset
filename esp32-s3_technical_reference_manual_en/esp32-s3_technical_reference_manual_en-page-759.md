**Title:**
Chapter 15 Permission Control (PMS)

**Register Information:**
- **Register Name:** PMS_CORE_O_DRAMO_PMS_MONITOR_1_REG (0x0108)
- **Bit Description and Values:**
  - `31` to `24`: Reserved
  - `23`: PMS CORE O DRAMO PMS MONITOR VIOLATE EN unauthorized. (R/W) [Set this bit to enable interrupt when CPUO's dBUS tries to access SRAM or ROM unauthorized]
  - `22`: PMS CORE O DRAMO PMS MONITOR VIOLATE_CLR
    - Description: Set this bit to clear the interrupt triggered when CPUO's dBUS tries to access SRAM or ROM unauthorized.
  - `21`: 
  - `20`: 
  - `19`: 
  - `18`: 
  - `17` to `0`: Reset

**Footer:**
- "Submit Documentation Feedback"
- Page number and document version information:
  - "ESP32-S3 TRM (Version 1.7)"
  - "GoBack"