**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Section Header:**
Register 12.20. TIMG_RTMTCALICFG2_REG (0x080)

**Table Description:**
- **Columns:** 
  - Offset in hex (e.g., "31", "7")
  - Bits
  - Description

**Table Content:**
- `TIMG_RTC_CALI_TIMEOUT`:
  - Offset: 31, Bit range: [7,6], Value: 0x1fffffff
  - Description: Indicates frequency calculation timeout. (RO)
  
- `TIMG_RTC_CALI_TIMEOUT_RST_CNT`:
  - Offset: 24, Bit range: [3,2], Value: 0
  - Description: Cycles to reset frequency calculation timeout. (R/W)

- `TIMG_RTC_CALI_TIMEOUT_THRES`:
  - Offset: 16, Bit range: [3,0], Value: 0
  - Description: Threshold value for the frequency calculation timer. If the timer’s value exceeds this threshold, a timeout is triggered. (R/W)

**Section Header:**
Register 12.21. TIMG_INT_ENA_TIMERS_REG (0x070)

**Table Description:**
- **Columns:** 
  - Offset in hex
  - Bits

**Table Content:**
- `TIMG_TX_INT_ENA`:
  - Offset: [3,2], Value: 0
  - Description: The interrupt enable bit for the TIMG_Tx_INT interrupt. (R/W)
  
- `TIMG_WDT_INT_ENA`:
  - Offset: [1,0], Value: 0
  - Description: The interrupt enable bit for the TIMG_WDT_INT interrupt. (R/W)

**Section Header:**
Register 12.22. TIMG_INT_RAW_TIMERS_REG (0x074)

**Table Description:**
- **Columns:** 
  - Offset in hex

**Table Content:**
- `TIMG_TX_INT_RAW`:
  - Offset: [3,2], Value: 0
  - Description: The raw interrupt status bit for the TIMG_Tx_INT interrupt. (R/WTC/SS)
  
- `TIMG_WDT_INT_RAW`:
  - Offset: [1,0], Value: 0
  - Description: The raw interrupt status bit for the TIMG_WDT_INT interrupt. (R/WTC/SS)

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:** 
669