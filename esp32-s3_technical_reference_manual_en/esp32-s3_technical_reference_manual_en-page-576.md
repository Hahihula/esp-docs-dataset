**Chapter Title:**
- Chapter 10 Low-power Management (RTC_CNTL)

**Menu/Navigation Link:**
- GoBack

**Body Text with List Items and Descriptions:**

- **bod_mode0_en:** RTC_CNTL_BROWN_OUT_ENA  
- **bod_mode0_rst_en:** RTC_CNTL_BROWN_OUT_RST_ENA
- **bod_mode0_rst_sel:** RTC_CNTL_BROWN_OUT_RST_SEL configures the reset type. For more information regarding Chip Reset and System Reset, please refer to 7 [Reset and Clock](#).
  - 0: resets the chip
  - 1: resets the system

- bod_mode1_sel: the first bit of RTC_CNTL_RTC_FIB_SEL.

- **bod_mode1_rst_en:** RTC_CNTL_BROWN_OUT_ANA_RST_EN

**Section Title with Subtitle and List Items under each Subtitle**

**Subtitle (10.4 Power Modes Management):**
- 10.4.1 Power Domain
  - ESP32-S3 has 10 power domains in three power domain categories:
    - **RTC**
      - Power management unit
      - RTC peripherals, including RTC GPIO, RTC I2C, Temperature Sensor, Touch Sensor, RTC ADC Controller, and ULP Coprocessor
    - **Digital**
      - Digital core
      - Wireless digital circuits
      - CPU
      - PD peripherals, including SPI2, GDMA, SHA, RSA, AES, HMAC, DS, and Secure Boot
    - **Analog**
      - Fast RC Oscillator (RC_FAST_CLK)
      - External Main Clock (XTAL_CLK)
      - Phase Lock Loop (PLL)
      - RF circuits

**Footer:**
- Espressif Systems 576 ESP32-S3 TRM (Version 1.7)  
- Submit Documentation Feedback