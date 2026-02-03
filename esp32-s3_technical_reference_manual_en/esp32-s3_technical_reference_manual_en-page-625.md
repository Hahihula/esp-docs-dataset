**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**GoBack Link:** GoBack

**Register Information:**
- **Register Name and Address:** Register 10.55, RTC_CNTL_RTC_XTAL32K_CONF_REG (0x00F8)
- Diagram Description:
  - The diagram shows a bit map for the register with labels such as "RTC_CNTL_XTAL32K_STABLE_THRES," "RTC_CNTL_XTAL32K_WDT_TIMEOUT," and others.
  - Bit positions are labeled from right to left starting at '0x' followed by hexadecimal values (e.g., 0x0, 0xff).

**Field Descriptions:**
1. **RTC_CNTL_XTAL32K_RETURN_WAIT:** Defines the waiting cycles before returning to the normal 32 kHz crystal oscillator.
   - Access Type: Read/Write
2. **RTC_CNTL_XTAL32K_RESETART_WAIT:** Defines the maximum waiting cycle before restarting the 32 kHz crystal oscillator.
   - Access Type: Read/Write
3. **RTC_CNTL_XTAL32K_WDT_TIMEOUT:** Defines the maximum waiting period for clock detection; if no clock is detected after this period, the 32 kHz crystal oscillator can be regarded as dead.
   - Access Type: Read/Write
4. **RTC_CNTL_XTAL32K_STABLE_THRES:** Defines the maximum allowed restarting period within which the 32 kHz crystal oscillator can be regarded as stable; if it is reached or exceeded, a reset will occur to restart the clock detection process again.
   - Access Type: Read/Write

**Footer Information:**
- **Company Name and Document Version:** Espressif Systems ESP32-S3 TRM (Version 1.7)
- Page Number: 625
- Link for Submitting Documentation Feedback