**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Header:**
Register 9.26. RTC_CNTL_VREG_REG (0x007C)

**Table:**
- RTC_CNTL_PREG_FORCE_PU, RTC_CNTL_DBOOST FORCE_PD, RTC_CNTL_DBIAS_WAK, RTC_CNTL_SCK_DCAP
- RTC_CNTL_DIG_VREG_DBIAS_WAK, RTC_CNTL_DIG_VREG_DBIAS_SLP

**Body Text with Descriptions and Registers:**

1. **RTC_CNTL_VREGFORCE_PPU**
   - Description: RTC voltage regulator - force power up.
   - Access Type (R/W)

2. **RTC_CNTL_VREGFORCE_PD**
   - Description: RTC voltage regulator - force power down
     - Note: In this case, it means decreasing the voltage to 0.8V or lower.

3. **RTC_CNTL_DBOOST FORCE_PU**
   - Description: RTC_DBOOST force power up.
   - Access Type (R/W)

4. **RTC_CNTL_DBOOST FORCE_PD**
   - Description: RTC_DBOOST force power down
   - Access Type (R/W)

5. **RTC_CNTL_DBIAS_WAK**
   - Description: RTC_DBIAS during wake-up.

6. **RTC_CNTL_DBIAS_SLP**
   - Description: RTC_DBIAS during sleep.
   - Access Type (R/W)

7. **RTC_CNTL_SCK_DCAP**
   - Description: Used to adjust the frequency of RTC slow clock
   - Access Type (R/W)

8. **RTC_CNTL_DIG_VREG_DBIAS_WAK**
   - Description: Digital voltage regulator DBIAS during wake-up.
   - Access Type (R/W)

9. **RTC_CNTL_DIG_VREG_DBIAS_SLP**
   - Description: Digital voltage regulator DBIAS during sleep
   - Access Type (R/W)

**Footer Information:**
- Page Number: 212
- Company Name: Espressif Systems
- Document Version and Link for Feedback:
  - ESP32 TRM (Version 5.6)
  - Submit Documentation Feedback