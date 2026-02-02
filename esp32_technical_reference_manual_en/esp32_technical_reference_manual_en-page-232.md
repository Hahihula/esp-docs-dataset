**Chapter Title:**
Chapter 10 Timer Group (TIMG)

**Section Header:**
Register 10.19. TIMGn_RTCCALICFG1_REG (0x006C)

**Field Description and Values:**
- **TIMGn_RTC_CALI_VALUE**: Calibration value when cycles of clock to be calibrated reach TIMGn_RTC_CALI_MAX, in unit of XTAL_CLK clock cycles.
  - **Binary Representation:** 0x00000
  - **Reset Value:** Reset

**Field Description and Values:**
- **Register 10.20. TIMGn_INT_ENA_REG (0x0098)**
  - **TIMGn_INT_WDT_INT_ENA**: The interrupt enable bit for the TIMGn_INT_WDT_INT interrupt.
    - **Access Type:** Read/Write
  - **TIMGn_INT_T1_INT_ENA**: The interrupt enable bit for the TIMGn_INT_T1_INT interrupt.
    - **Access Type:** Read/Write (R/W)
  - **TIMGn_INT_TO_INT_ENA**: The interrupt enable bit for the TIMGn_INT_TO_INT interrupt.

**Field Description and Values:**
- **Register 10.21. TIMGn_INT_RAW_REG (0x009c)**
  - **TIMGn_INT_WDT_INT_RAW**: The raw interrupt status bit for the TIMGn_INT_WDT_INT interrupt.
    - **Access Type:** Read Only
  - **TIMGn_INT_T1_INT_RAW**: The raw interrupt status bit for the TIMGn_INT_T1_INT interrupt.
    - **Access Type:** Read Only (RO)
  - **TIMGn_INT_TO_INT_RAW**: The raw interrupt status bit for the TIMGn_INT_TO_INT interrupt.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Information:**
ESP32 TRM (Version 5.6)